<script>
  import Table from "sveltestrap/src/Table.svelte";

  const tableHeading = ["Type", "Title", "👁", "🧑🏿"];
  const tableData = [
    { title:"Computer Engineering 3", type: "Lecture", views: 210, percentage: 91 },
    { title:"Filmography Primer", type: "Video", views: 190, percentage: 85 },
    { title:"Linux Networking Basics", type: "Page", views: 154, percentage: 79 },
    { title:"Expanded Set theory", type: "Lecture", views: 144, percentage: 69 },
  ];


</script>

<Table responsive>
  <thead>
    <tr>
      {#each tableHeading as heading}
        <th>{heading}</th>
      {/each}
    </tr>
  </thead>

  <tbody>
    {#each tableData as data}
      <tr>
        <td>{data.type}</td>
        <th scope="row">{data.title}</th>
        <td>{data.views}</td>
        <td>{data.percentage}%</td>
      </tr>
    {/each}
  </tbody>
</Table>
