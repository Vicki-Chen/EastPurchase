<template>
    <div>
        <Header></Header>
        <Nav></Nav>
        <Banner></Banner>
        <ProductList></ProductList>
        <Footer></Footer>
    </div>
</template>

<script type="text/javascript">
import Header from '../../commons/Header';
import Nav from '../../commons/Nav';
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
        Header,Nav,Banner,ProductList,Footer
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->

