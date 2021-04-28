<template>
  <div ref="resizeRef">
    <svg ref="svgRef">
      <g class="x-axis" />
      <g class="y-axis" />
    </svg>
  </div>
</template>

<script>
import { onMounted, ref, watchEffect } from "vue";
import {
  select,
  line,
  scaleLinear,
  min,
  max,
  curveBasis,
  axisBottom,
  axisLeft,
} from "d3";
import useResizeObserver from "./ResizeObserver";

export default {
  name: "BarChart",
  props: ["data"],
  setup(props) {
    const svgRef = ref(null);
    const { resizeRef, resizeState } = useResizeObserver();

    onMounted(() => {
      const svg = select(svgRef.value);

      watchEffect(() => {
        const { width, height } = resizeState.dimensions;
        const xScale = scaleLinear()
          .domain([0, props.data.length - 1])
          .range([0, width]);

        const yScale = scaleLinear()
          .domain([min(props.data), max(props.data)])
          .range([height, 0]);

        const lineGen = line()
          .curve(curveBasis)
          .x((value, index) => xScale(index))
          .y((value) => yScale(value));

        svg
          .selectAll(".line")
          .data([props.data])
          .join("path")

          .attr("class", "line")
          .attr("stroke", "#888")
          .attr("d", lineGen);

        const xAxis = axisBottom(xScale);
        svg
          .select(".x-axis")
          .style("transform", `translateY(${height}px)`)
          .call(xAxis);

        const yAxis = axisLeft(yScale);
        svg.select(".y-axis").call(yAxis);
      });
    });

    return { svgRef, resizeRef };
  },
};
</script>

<style scoped>
svg {
  background: #17fc03;
  color: #fff;
  display: block;
  fill: none;
  height: 100%;
  overflow: visible;
  stroke: none;
  width: 100%;
}
</style>
