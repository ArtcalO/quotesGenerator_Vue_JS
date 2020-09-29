<template>
	<div class="quote-card">
		<div>
			<div >
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

<style >
	
	.quote-card{
		width: 30%;
		height: 50px;
		margin-right: 20px;
		text-align: center;
		padding-top: 8px;
		margin-top: 10px;
		background-color: gray;
	}
	.quote-card:hover{
		cursor:pointer;
		background-color: orange;
	}

</style>