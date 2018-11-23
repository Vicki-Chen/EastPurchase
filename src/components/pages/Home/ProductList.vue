<template>
	<div id="ProductList">
		<ul>
			<li v-for="(item,index) in arr" :key="index">
				<img :src="item.item_image"/>
				<div class="line">
					
				</div>
			</li>
		</ul>
	</div>
</template>

<script>
	export default {
		name:"ProductList",
		components:{},
		data(){
			return {
				title:"我是ProductList",
				arr:[]
			}
		},
		methods:{
			fn(){
				this.$axios.get("/api/mt/commonCornersData?shop_num=7781&corner_nums%5B%5D=9541&corner_nums%5B%5D=11221&corner_nums%5B%5D=9544&corner_nums%5B%5D=9545&corner_nums%5B%5D=9681&corner_nums%5B%5D=11161&corner_nums%5B%5D=12081")
				.then((res)=>{
//					console.log(res);
					this.arr=res.data[4].setList[1].contentList;
					console.log(this.arr);
					
	           	})
				.catch((err)=>{
	           		console.log(err)
	           	})
			}	
		},
		created(){
			this.fn();
		}
	}
</script>

<style lang="less" scoped="scoped">
	@import url('../../../styles/main.less');
	#ProductList{
		.top(252);
		ul{
			.padding(0,10,10,10);
			.margin(5,0,0,0);
			li{
				float:left;
				list-style: none;
				.h(130);
				.w(81.6);
				background:#dadada;
				box-sizing:border-box;
				position:relative;
				.margin(3,3,3,3);
				img{
					.h(130);
					.w(81.6);
				}
				.line{
					width:0;
					.h(62);
					border-right:#c2c2c2 1px solid;
					position:absolute;
					.top(0);
					.right(0);
					.margin(46,0,0,0);
				}
			}
		}
	}
	#ProductList::after{
		overflow:hidden;
		display:block;
		visibility: hidden;
		height:0;
		content: '';
		clear:both;
	}
	
</style>