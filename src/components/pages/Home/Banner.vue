<template>
    <div class='banner'>
        <div class="swiper-container">
		    <div class="swiper-wrapper">
	        	<div class="swiper-slide" v-for="(item,index) in arr" :key='index'>
	        		<img class='img1' :src="item.item_image" >
	        	</div>
		    </div>	    
		    <!-- 如果需要滚动条 -->
			<div class="swiper-pagination"></div>
		</div>
    </div>
</template>

<script>
	import '../../../../static/swiper.min.js';
    import Swiper from 'swiper';
    export default{
        name:'Banner',
        components:{},
        data(){
            return{
                name:'baaner',
				arr:[]
	            }
        },
        created(){
        	this.fn();	
		},
		mounted(){
			
			
		},
		methods: {
			fn(){
				this.$axios.get("/api/mt/commonCornersData?shop_num=7781&corner_nums%5B%5D=9541&corner_nums%5B%5D=11221&corner_nums%5B%5D=9544&corner_nums%5B%5D=9545&corner_nums%5B%5D=9681&corner_nums%5B%5D=11161&corner_nums%5B%5D=12081")
				.then((res)=>{
//					console.log(res);
					this.arr=res.data[0].setList[0].contentList;
					console.log(this.arr);
					//轮播图
					this.$nextTick(()=>{
						var mySwiper = new Swiper('.swiper-container', {
							loop: true, // 循环模式选项
							autoplay:true,
							// 如果需要分页器
						    pagination: {
						      el: '.swiper-pagination',
						    }
						})
					})
	           	})
				.catch((err)=>{
	           		console.log(err)
	           	})
	      	}			
		}
    }
</script>
<style lang="less" scoped>
@import url('../../../styles/main.less');
@import '../../../../static/swiper.min.css';
.banner{
	width: 100%;
    .h(158);
    .margin(94,0,0,0);
    .swiper-wrapper{
    	.swiper-slide{
	        width: 100%;
	        .h(158);
	        .img1{
		        width:100%;
		        .h(158);
		    }
	    }
    }  
}
</style>

