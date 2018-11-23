<template>
	<div id="Footer">
		<ul>
			<router-link to='/' tag='li' v-for='(item,index) in arrNav' active-class="active" :key='index' >{{item}}</router-link>
		</ul>
	</div>
</template>

<script>
	export default {
		name:"Footer",
		components:{},
		data(){
			return {
				title:"我是导航",
				arrNav:['首页','团购','全球购','商城']
			}
		}
	}
</script>

<style lang="less" scoped="scoped">
	@import url('../../styles/main.less');
	#Footer{
		ul{
			display:flex;
			.h(40);
			li{
				
				list-style: none;
				flex:1;
				.h(40);
				color:#888;
				.lh(40);
				text-align:center;
				box-sizing:border-box;
				border-bottom:1px solid #dadada;
				.fs(16);
			}
			.active{
				border-bottom:3px solid red;
				color:red;
			}
		}
	}
</style>