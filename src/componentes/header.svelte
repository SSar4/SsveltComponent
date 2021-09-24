<script>
  import { onMount } from "svelte";

  export let url 
  let uf = [];

  onMount(async function() {
    const response = await fetch(url);
    const json = await response.json();
    uf = json;
  });
</script>

<slot {uf}/>