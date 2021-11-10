<script>
  import { onMount } from "svelte";
  import Chart from "chart.js";

  let barChart;

  const chartData = {
    labels: ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday", "Sunday"],
    datasets: [
      {
        label: "minutes per student",
        data: [50, 65, 70, 60, 50, 35, 25],
        backgroundColor: "rgba(3,117,220)"
      }
    ]
  };
  const chartOptions = {
    scales: {
      yAxes: [
        {
          ticks: {
            beginAtZero: true
          }
        }
      ]
    }
  };

  function createChart() {
    var ctx = barChart;
    var myChart = new Chart(ctx, {
      type: "bar",
      data: chartData,
      options: chartOptions
    });
  }

  onMount(createChart);
</script>

<canvas bind:this={barChart} />
