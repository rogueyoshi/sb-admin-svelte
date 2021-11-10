<script>
  import Table from "sveltestrap/src/Table.svelte";

  const tableHeading = ["Name", "Earnings"];
  const tableData = [
    { name: "@door_to_tomorrow", score: "3000" },
    { name: "@underdogs_secret", score: "2700" },
    { name: "@winning_formula", score: "2550" },
    { name: "@wings_to_discovery", score: "2400" }
  ];


</script>

<Table responsive>
  <tbody>
    {#each tableData as data}
      <tr>
        <th scope="row">{data.name}</th>
        <td>{data.score}</td>
      </tr>
    {/each}
  </tbody>
</Table>
