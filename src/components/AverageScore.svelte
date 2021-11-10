<script>
  import Table from "sveltestrap/src/Table.svelte";

  const tableHeading = ["Name", "Score"];
  const tableData = [
    { name: "Mark", score: "9.3" },
    { name: "Jacob", score: "8.7" },
    { name: "Jacob", score: "8.7" },
    { name: "Jacob", score: "8.7" },
    { name: "Jacob", score: "8.7" },
    { name: "Larry", score: "8.7" }
  ];


</script>

<Table bordered responsive>
  <tbody>
    {#each tableData as data}
      <tr>
        <td>{data.name}</td>
        <td>{data.score}</td>
      </tr>
    {/each}
  </tbody>
</Table>
