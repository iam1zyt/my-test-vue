<template>
  <div class="content">
    <div class="nav">
      <OptionHeader />
      <OpCenter />
    </div>
  </div>
</template>

<script>
import OptionHeader from "./OptionHeader.vue";
import OpCenter from "./OpCenter.vue";
export default {
  name: "Option4",
  components: { OptionHeader, OpCenter },
  data() {
    return {
      piedata: [
        { value: 1048, name: "Search Engine" },
        { value: 735, name: "Direct" },
        { value: 580, name: "Email" },
        { value: 484, name: "Union Ads" },
        { value: 300, name: "Video Ads" },
      ],
      scatterData:[
         [
        [10.0, 8.04],
        [8.0, 6.95],
        [13.0, 7.58],
        [9.0, 8.81],
        [11.0, 8.33],
        [14.0, 9.96],
        [6.0, 7.24],
        [4.0, 4.26],
        [12.0, 10.84],
        [7.0, 4.82],
        [5.0, 5.68],
      ],
      [
        [10.0, 9.14],
        [8.0, 8.14],
        [13.0, 8.74],
        [9.0, 8.77],
        [11.0, 9.26],
        [14.0, 8.1],
        [6.0, 6.13],
        [4.0, 3.1],
        [12.0, 9.13],
        [7.0, 7.26],
        [5.0, 4.74],
      ],
      [
        [10.0, 7.46],
        [8.0, 6.77],
        [13.0, 12.74],
        [9.0, 7.11],
        [11.0, 7.81],
        [14.0, 8.84],
        [6.0, 6.08],
        [4.0, 5.39],
        [12.0, 8.15],
        [7.0, 6.42],
        [5.0, 5.73],
      ],
      [
        [8.0, 6.58],
        [8.0, 5.76],
        [8.0, 7.71],
        [8.0, 8.84],
        [8.0, 8.47],
        [8.0, 7.04],
        [8.0, 5.25],
        [19.0, 12.5],
        [8.0, 5.56],
        [8.0, 7.91],
        [8.0, 6.89],
      ],
      ]
    };
  },
   created() {
      this.setData();
    },
    methods: {
      setData(){
        this.$store.commit('setPieData',this.piedata);
        this.$store.commit('setScatterData',this.scatterData)
      }
    },
};
</script>

<style scoped>
</style>