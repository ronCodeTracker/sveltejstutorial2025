
<!-- java script code -->
<script lang="ts">
   let { 
	   name,	   
   }:{
     name: string;     
   }
   = $props();
</script>

<!-- html svelte.js type -->
<div>
  {#if name}
	<h1>{name}'s Form</h1>
  {/if}
</div>
<hr>
<!-- ----------------- -->


<!-- css styling  -->
<style>
  h1 {
	color: green;
  }
</style>





