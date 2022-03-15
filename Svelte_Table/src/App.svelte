<script>
  import PeopleTable from "./components/peopleTable/PeopleTable.svelte";
</script>

<main>
  <div id="table-container">
    <PeopleTable id="peopleTable" />
    <div id="footer">By Raszbanana</div>
  </div>

</main>

<style>
  main {
    text-align: center;
    background-color: #689d0d;
  }

  #table-container {
	  border-style:groove; 
  }

  #footer {
    margin-top: 30px;
  }
</style>
