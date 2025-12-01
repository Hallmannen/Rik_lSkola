<script>
	import favicon from '$lib/assets/favicon.svg';

	let { children } = $props();
	import { base } from '$app/paths';
	
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
	
</svelte:head>



<nav>
	<a href="{base}/">hem</a> 

	<a href="{base}/Photoapp">Photo App</a> 
	<a href="{base}/register">Register</a>
	<a href="{base}/shoppinglist">shoppinglist</a>
</nav>



{@render children?.()}
<style>
	
:global(body), :global(html){
  margin: 0%;
  padding: 0%;
  height: 100vh;
  width: 100vw;
  display: grid;
 
        
}    

</style>