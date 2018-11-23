<template>
    <div>
        <Header></Header>
    </div>
</template>

<script type="text/javascript">
import Header from '../../commons/Header';
export default {
    name: 'Home',
    data() {
        return {
            msg: 'Home'
        }
    },
    components:{
        Header
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->

