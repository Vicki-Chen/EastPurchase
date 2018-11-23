<template>
	<div class="swiper-container">
	    <div class="swiper-wrapper">
		    <div class="swiper-slide" v-for="(item,index) of list">
		    	<img :src="item.item_image">
		    	<p>
		    		<span>{{item.alt_desc}}</span>
		    		<span>{{item.conts_desc}}</span>
		    	</p>
		    </div>
	    </div>
    	<div class="swiper-pagination"></div>
	</div>
</template>

<script type="text/javascript">
	import Swiper from '../../../../static/swiper.min.js';
	import Vue from 'vue';
	export default{
		name: "HomeBanner",
		data(){
			return{
				list:[],
			}
		},
		methods:{
			getData(){
				this.$axios.get('/api/mt/commonCornersData?shop_num=7781&corner_nums%5B%5D=9541&corner_nums%5B%5D=11221&corner_nums%5B%5D=9544&corner_nums%5B%5D=9545&corner_nums%5B%5D=9681&corner_nums%5B%5D=11161&corner_nums%5B%5D=12081&auth_key=&prev_yn=N&prev_std_dt=&seq_shop_num=&prev_seq_temp_num=')
				.then((res)=>{
					// console.log(res.data[3].setList[0].contentList);
					this.list = res.data[3].setList[0].contentList;
					Vue.nextTick(()=>{
					    this.swiper = new Swiper('.swiper-container', {
						    slidesPerView: 1,
						    spaceBetween: 0,
						    pagination: {
						        el: '.swiper-pagination',
						        clickable: true,
						    },
						});
					})
					
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
	@import url('../../../../static/swiper.min.css');
	.swiper-slide{
		border:1px solid #ccc;
		img{
			.w(375);
			.h(190);
		}
		p{
			display: flex;
			.margin(10,10,10,10);
			justify-content: space-between;
			.fs(16);
			span:nth-child(2){
				color:red;
			}
		}
	}
</style>
