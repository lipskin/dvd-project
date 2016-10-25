<template>
  <chart :options="lineData"></chart>
</template>

<style scoped>
.echarts {
  height: 300px;
}



</style>

<script>

export default {
  data() {
    return {
      lineData: {
        title: {
          text: 'EC2',
        },
        tooltip: {
          trigger: 'axis',
        },
        legend: {
          data: ['EC2 running Linux/UNIX', 'EBS'],
        },
        toolbox: {},
        grid: {
          left: '3%',
          right: '4%',
          bottom: '3%',
          containLabel: true,
        },
        xAxis: [
          {
            type: 'category',
            boundaryGap: false,
            data: ['MON', 'TUE', 'WEN', 'THU', 'FRI', 'SAT', 'SUN'],
          },
        ],
        yAxis: [
          {
            type: 'value',
          },
        ],
        series: [
          {
            name: 'EBS',
            type: 'line',
            stack: 'total',
            areaStyle: { normal: { color: 'rgba(255, 138, 128, 1)' } },
            data: [120, 132, 101, 134, 90, 230, 210],
          },
          {
            name: 'EC2 running Linux/UNIX',
            type: 'line',
            stack: 'total',
            /* label: {
              normal: {
                show: true,
                position: 'top',
              },
            }, */
            areaStyle: { normal: { color: 'rgba(128, 216, 255, 1)' } },
            data: [220, 182, 191, 234, 290, 330, 310],
          },
        ],
      },
    };
  },
};

</script>
