<template>
	<div>
		<ul>
			<li v-for='(item,index) of list' :key="index">
				<img :src="item.item_image">
				<div class="box">
					<h4>{{item.item_name}}</h4>
					<div>
						<p>
							<b>￥{{item.last_sale_price}}</b>
							<s v-if="item.cust_price?true:false">￥{{item.cust_price}}</s>
						</p>
						<P v-if="item.cust_price?true:false">{{item.co_dc}}折</P>
					</div>
					
				</div>
			</li>
		</ul>
	</div>
</template>

<script type="text/javascript">
	export default{
		name: "HomeGoods",
		data(){
			return{
				list:[],
			}
		},
		methods:{
			getData(){
				this.$axios.get('/api/mt/commonCornersData?shop_num=7781&corner_nums%5B%5D=9541&corner_nums%5B%5D=11221&corner_nums%5B%5D=9544&corner_nums%5B%5D=9545&corner_nums%5B%5D=9681&corner_nums%5B%5D=11161&corner_nums%5B%5D=12081&auth_key=&prev_yn=N&prev_std_dt=&seq_shop_num=&prev_seq_temp_num=')
				.then((res)=>{
					console.log(res.data[2].setList[0].contentList);
					this.list = res.data[2].setList[0].contentList;
				})	
				.catch((err)=>{
					console.log(err);
				})
			}
		},
		created(){
			this.getData()
		}
	}
</script>

<style type="text/css" lang="less" scoped>
	@import url('../../../styles/main.less');
	ul{
		.padding(20,0,0,0);
		background-color: #ccc;
		li{
			background-color: #fff;
			.w(375);
			.h(245);
			.fs(16);
			.margin(10,0,0,0);
			text-align:center;
			img{
				.w(170);
				.h(170)
			}
			.box{
				border-top: 1px solid #ccc;
				text-align:left;
				.padding(10,10,10,10);
				p{
					.margin(0,0,5,0);
					color: red;
					s{
						text-decoration: line-through;
						.fs(14);
					}
				}
				div{
					display: flex;
					justify-content: space-between;
				}
			}
		}
	}
</style>