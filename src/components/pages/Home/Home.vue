<template>
    <div>
        <Header></Header>
        <Nav></Nav>
    </div>
</template>

<script type="text/javascript">
import Header from '../../commons/Header';
import Nav from '../../commons/Nav';
export default {
    name: 'Home',
    data() {
        return {
            msg: 'Home'
        }
    },
    components:{
        Header,Nav
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->

