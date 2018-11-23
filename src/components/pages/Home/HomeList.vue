<template>
	<div>
		<ul class="cleanfix">
			<router-link to='/' tag="li" v-for="(item,index) of list">
				<img :src="item.contentList[0].item_image">
				<p>
					{{item.contentList[0].conts_desc}}
				</p>
			</router-link>
		</ul>
	</div>
</template>

<script type="text/javascript">
	export default{
		name: "HomeList",
		data(){
			return{
				url:'/api/mt/commonCornersData?shop_num=7781&corner_nums%5B%5D=9541&corner_nums%5B%5D=11221&corner_nums%5B%5D=9544&corner_nums%5B%5D=9545&corner_nums%5B%5D=9681&corner_nums%5B%5D=11161&corner_nums%5B%5D=12081&auth_key=&prev_yn=N&prev_std_dt=&seq_shop_num=&prev_seq_temp_num=',
				list:'',
				
			}
		},
		methods: {
			getList(){
				this.$axios.get(this.url,this.data)
				.then((res)=>{
					// console.log(res.data[1].setList,36);
					this.list = res.data[1].setList
				})
				.catch((err)=>{
					console.log(err,39);
				})
			}
		},
		created(){
			this.getList()
		}
	}
</script>

<style type="text/css" lang="less" scoped>
@import url('../../../styles/main.less');
	ul{
		width:100%;
		.fs(14);
		li{
			text-align: center;
			.margin(12,0,0,0);
			float:left;
			width:20%;
			img{
				.w(45);
				.h(45);
			}
		}
	}
	.cleanfix::after{
		content:'';
		clear:both;
		display: block;
		height:0;
		visibility: hidden;
		overflow:hidden;

	}
</style>