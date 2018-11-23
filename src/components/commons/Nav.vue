<template>
	<div id="Nav">
		<ul>
			<router-link to='/' tag='li' v-for='(item,index) in arrNav' active-class="active" :key='index' >{{item}}</router-link>
		</ul>
	</div>
</template>

<script>
	export default {
		name:"Nav",
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
	#Nav{		
		ul{
			display:flex;
			.h(40);
			position:fixed;
			.top(54);
			.left(0);
			right:0;
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
	#Nav:after {
	    content: "020";
	    display: block;
	    height: 0;
	    visibility: hidden;
	    clear: both;
	    overflow:hidden;
	    
	}
	.clearfix {
	    zoom: 1;
	}
</style>