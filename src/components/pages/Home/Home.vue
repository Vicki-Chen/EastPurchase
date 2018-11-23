<template>
    <div>
        <Header></Header>
        <Nav></Nav>
        <HomeList></HomeList>
        <HomeBanner></HomeBanner>
        <HomeGoods></HomeGoods>
    </div>
</template>

<script type="text/javascript">
import Header from '../../commons/Header';
import Nav from '../../commons/Nav';
import HomeList from './HomeList';
import HomeBanner from './HomeBanner';
import HomeGoods from './HomeGoods';
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
        HomeGoods
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->

