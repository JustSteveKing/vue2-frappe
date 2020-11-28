<template>
  <div id="app">
    <vue-frappe
      id="test"
      title="Monthly Distribution"
      type="heatmap"
      :colors="['#ebedf0', '#c0ddf9', '#73b3f3', '#3886e1', '#17459e']"
      :discreteDomains="false"
      :height="300"
      :dataPoints="data"
      :startDate="start"
      :endDate="end"
    ></vue-frappe>
    <!-- You can add continuously as a prop to allow for a continous distribution of heat squares (as on GitHub),
    rather than showing the month-wise separation. -->
  </div>
</template>

<script>
export default {
  name: "App",
  computed: {
    start() {
      let date = new Date();

      date.setMonth(2);

      return date;
    },
    end() {
      let date = new Date();

      date.setMonth(6);

      return date;
    },
    data() {
      let date1 = new Date();
      let date2 = new Date();
      let date3 = new Date();

      date1.setMonth(2).toTimeString;
      date2.setMonth(3).toTimeString;
      date3.setMonth(4).toTimeString;

      return {
        date1: 30,
        date2: 50,
        date3: 150,
      };
    },
  },
};
</script>