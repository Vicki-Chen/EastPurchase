<template>
	<div class="head">
		{{test}}
	</div>
</template>

<script type="text/javascript">
	export default {
		name: "Header",
		data(){
			return {
				test: "Head"
			}
		},
	}
</script>

<style lang="less" scoped>
	@import url('../../styles/main.less');
	.head{
		.h(54);
		width:100%;
		background-color: #f12e24;
		
	}
</style>