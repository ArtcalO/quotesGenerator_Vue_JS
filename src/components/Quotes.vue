<template>
		<div>
			<div class="card text-center m-3 quote-card" style="width: 19rem;">
			  <div class="card-body">
			  	<slot></slot>
			  </div>
			</div>
		</div>
</template>

<script>
	export default{
		props : ['quotes']
	};
</script>

<style scoped>
	.quote-card:hover{
		cursor: pointer;
		background-color: rgb(37,9,86);
		color: white;
	}
</style>