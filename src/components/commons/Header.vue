<template>
	<div class="head">
		<i class="fa fa-bars" aria-hidden="true"></i>
		<img src="http://m.ocj.com.cn/common/mobile_phone/cssimage/indeximg/logoicon.png" />
		<input type="" name="" value="搜索货号/关键词">
		<i class="fa fa-search" aria-hidden="true"></i>
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
		position: relative;
		.fs(24);
		color: #fff;
		display: flex;
		justify-content: space-around;
		align-items: center;
		.h(54);
		width:100%;
		background-color: #f12e24;
		img{
			.w(35);
			.h(35)
		}
		input{
			.w(267);
			.h(32);
			color: #fff;
			background-color: #d42e2c;
		    border: 1px solid #d42e2c;
		    padding-left: 10px;
		    .fs(18);
		}
		.fa-search{
			position: absolute;
			right:14px;
			.fs(18);
		}
	}
</style>