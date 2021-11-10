<script>
  import Breadcrumb from "sveltestrap/src/Breadcrumb.svelte";
  import BreadcrumbItem from "sveltestrap/src/BreadcrumbItem.svelte";
  import Card from "sveltestrap/src/Card.svelte";
  import CardBody from "sveltestrap/src/CardBody.svelte";
  import CardHeader from "sveltestrap/src/CardHeader.svelte";
  import CardText from "sveltestrap/src/CardText.svelte";
  import CardSubtitle from "sveltestrap/src/CardSubtitle.svelte";
  import Row from "sveltestrap/src/Row.svelte";

  import DashboardCard from "../components/DashboardCard.svelte";
  import CustomCard from "../components/CustomCard.svelte";
  import Table from "../components/Table.svelte";
  import AreaChart from "../components/Charts/AreaChart.svelte";
  import BarChart from "../components/Charts/BarChart.svelte";
  import AverageActivity from "../components/Charts/AverageActivity.svelte";
import AverageScore from "../components/AverageScore.svelte";

  let title = "Admin Panel";
</script>

<svelte:head>
  <title>{title}</title>
</svelte:head>
<h1 class="mt-4">Dashboard</h1>
<Breadcrumb class="mb-4">
  <BreadcrumbItem active>STEM Activities</BreadcrumbItem>
</Breadcrumb>
<Row>
  <div class="col-xl-3 col-md-6">
    <CustomCard cardTitle="122" cardIcon="fas fa-users">
      Registered Students
    </CustomCard>
  </div>
  <div class="col-xl-3 col-md-6">
    <CustomCard cardTitle="6.8 (+12%)" cardIcon="fas fa-chart-area">
      Average Mastery
    </CustomCard>
  </div>
  <div class="col-xl-3 col-md-6">
    <CustomCard cardTitle="12 (10%)" cardIcon="fas fa-level-down-alt">
      Underperforming Students
    </CustomCard>
  </div>
  <div class="col-xl-3 col-md-6">
    <CustomCard cardTitle="83%" cardIcon="fas fa-book">
      Of latest activities completed
    </CustomCard>
  </div>
</Row>
<Row>
  <div class="col-xl-6">
    <CustomCard cardTitle="Students' Average Activity" cardIcon="fas fa-chart-area">
      <AverageActivity />
    </CustomCard>
  </div>
  <div class="col-xl-3">
  <CustomCard cardTitle="Students' Average Score" cardIcon="fas fa-table">
    <AverageScore />
  </CustomCard>
  </div>
  <div class="col-xl-3">
    <CustomCard cardTitle="Top Engagements" cardIcon="fas fa-table">
      <ul>
        <li>
          Lecture: Computer Engineering 3 (230 Views, 91%)
        </li>
        <li>
          Video: Introduction to Programming (190 Views, 85%)
        </li>
        <li>
          Page: Applied Algebra (154 Views, 79%)
        </li>
      </ul>
    </CustomCard>
  </div>
</Row>

<Row>
  <div class="col-xl-3 col-md-6">
    <CustomCard cardTitle="4" cardIcon="fas fa-users">
      Days until next assignments
    </CustomCard>
  </div>
  <div class="col-xl-3 col-md-6">
    <CustomCard cardTitle="32" cardIcon="fas fa-chart-area">
      Average total hours spent
    </CustomCard>
  </div>
</Row>
