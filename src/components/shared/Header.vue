<template>
	<div>
		<div class="jumbotron text-center">
		  <h1>Quote Generator in Vue JS</h1>
		  <p>Write a Quote and Post It</p>
		</div>

		<div class="progress"  style="height:40px">
		  <div class="progress-bar progress-bar-striped" :style="{width: (quotes.length / max) * 100 + '%'}" style="height:40px">{{ quotes.length }} / {{max}}</div>
		</div> 
	</div>
</template>
<script >
	export default {
		props : ['quotes','max']
	};
</script>

<style>
	
</style>