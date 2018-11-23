<template>
    <div>
        <Header></Header>
        <Nav></Nav>
        <Footer></Footer>
    </div>
</template>

<script type="text/javascript">
import Header from '../../commons/Header';
import Nav from '../../commons/Nav';
import Footer from '../../commons/Footer';
export default {
    name: 'Home',
    data() {
        return {
            msg: 'Home'
        }
    },
    components:{
        Header,Nav,Footer
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->

