<script>
  import { onMount } from 'svelte';
  import jQuery from 'jquery';

  onMount(async function () {
      let number = Math.floor(Math.random() * (1000 - 1)) + 1;
      jQuery("#randnumber").html("<em>"+ number +"</em>");

      console.log("hallo")
      const response = await fetch("http://localhost:7878/allareas");
      const data = await response.json();
      console.log(data)
    }
  )
</script>

<main>
  <h3>Raumplaner</h3>
  <p>Übersicht</p>
  <div id="randnumber"></div>
</main>
<style>

</style>
