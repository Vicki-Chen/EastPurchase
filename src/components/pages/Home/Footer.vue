<template>
	<div id="Footer">
		2004-2018 ocj.com.cn All Rights Reserved
	</div>
</template>

<script>
	export default{
		name:"Footer",
		components:{},
		data(){
			return {
				title:"我是Footer",
				
			}
		}
	}
</script>

<style lang="less" scoped="scoped">
	@import url('../../../styles/main.less');
	#Footer{
		.h(35);
		background:#ebebeb;
		color:#000;
		.padding(10,0,10,0);
		text-align:center;
		.fs(12);
	}
</style>
