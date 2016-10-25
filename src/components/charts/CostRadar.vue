<template>
  <chart :options="radarData"></chart>
</template>

<style scoped>

</style>

<script>

export default {
  data() {
    return {
      radarData: {
        title: {
          text: 'Cost Radar',
        },
        tooltip: {},
        legend: {
          data: ['Actual Spending'],
        },
        radar: {
          // shape: 'circle',
          indicator: [
           { name: 'EC2', max: 30000 },
           { name: 'RDS', max: 30000 },
           { name: 'ELB', max: 30000 },
           { name: 'S3', max: 30000 },
           { name: 'Other', max: 30000 },
          ],
        },
        series: [{
          name: 'Cost',
          type: 'radar',
          // areaStyle: {normal: {}},
          data: [
            {
              value: [26000, 14000, 18000, 11000, 22000],
              name: 'Actual Cost',
            },
          ],
        }],
      },
    };
  },
};

</script>
