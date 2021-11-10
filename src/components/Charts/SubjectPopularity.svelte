<script>
  import Chart from "chart.js";
  import { onMount } from "svelte";

  const chartData = {
    labels: ["Character Development", "Health & Wellness", "Esports", "STEM", "Stewardship"],
    datasets: [
      {
        data: [120, 190, 300, 500, 200],
        backgroundColor: [
          "rgba(255, 99, 132, 0.8)",
          "rgba(54, 162, 235, 0.8)",
          "rgba(255, 206, 86, 0.8)",
          "rgba(75, 192, 192, 0.8)",
          "rgba(153, 102, 255, 0.8)",
          "rgba(255, 159, 64, 0.8)"
        ],
        borderColor: "white",
        borderWidth: 1
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
    var ctx = document.getElementById("pieChart");
    var myChart = new Chart(ctx, {
      type: "pie",
      data: chartData,
      options: chartOptions
    });
  }

  onMount(createChart);
</script>

<canvas id="pieChart" />
