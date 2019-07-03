<template>
<div>
    <h1>{{count}}</h1>
    <button @click="add">增</button>  
</div>
    
</template>

<script>
import {mapState,mapActions} from 'vuex'
export default {
    data() {
        return {
            // count:null
        }
    },
    computed:{
        ...mapState({
            count: state => state.count
        })
    },
    methods: {
        ...mapActions({
            add: 'increment'
        })
    },
}
</script>

