<script>
	import Header from "./componentes/header.svelte";
	const props = {
		url: "https://servicodados.ibge.gov.br/api/v1/localidades/estados",
		title: "A list of todos",
	};
</script>

<main>
	<Header  {...props} let:uf>
		<h1>lista de uf brasileiros</h1>
		<ul>
			{#each uf as nome}
			  <li>{nome.nome}</li>
			{/each}
		  </ul>
	</Header>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
      li{
        list-style: none;
      }

</style>
