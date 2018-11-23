<template>
    <div>
        <Header></Header>
        <Nav></Nav>
		 <Banner></Banner>
        <HomeList></HomeList>
		<ProductList></ProductList>
        <HomeBanner></HomeBanner>
        <HomeGoods></HomeGoods>
        <Footer></Footer>
    </div>
</template>

<script type="text/javascript">
import Header from '../../commons/Header';
import Nav from '../../commons/Nav';
import HomeList from './HomeList';
import HomeBanner from './HomeBanner';
import HomeGoods from './HomeGoods';
import Banner from './Banner';
import ProductList from './ProductList';
import Footer from './Footer';
export default {
    name: 'Home',
    data() {
        return {
            msg: 'Home'
        }
    },
    components:{
        Header,
        Nav,
        HomeList,
        HomeBanner,
        HomeGoods,Banner,ProductList,Footer
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->

