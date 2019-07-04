<template>
<div>
    <h3>monment</h3>
    {{date}}
    <h1>{{count}}</h1>
    <button @click="add">增</button>  
</div>
    
</template>

<script>
import {mapState,mapActions} from 'vuex'
import moment from 'moment'

import {Vue, Component,Emit, Watch} from 'vue-property-decorator'
import {
  State,
  Getter,
  Action,
  Mutation,
  namespace
} from 'vuex-class'

// const store = namespace('@/store')
@Component

export default class One extends Vue {
    @Action('increment') add
    get date() {
        return moment().startOf('hour').subtract(1, 'hour');
    }
    // date = s
    get count(){ 
        return this.$store.state.count
    }
    // computed = {
    //     ...mapState({
    //         count: state => state.count
    //     })
    // }
    // add(){
    //     debugger
    //     this.$store.dispatch('increment')
    // }
    // ...mapActions({
    //         add: 'increment'
    //     })
    // }
    
}

// export default {
//     data() {
//         return {
//             // count:null
//             date:moment().startOf('hour').subtract(1, 'hour')
//         }
//     },
//     computed:{
//         ...mapState({
//             count: state => state.count
//         })
//     },
//     methods: {
//         ...mapActions({
//             add: 'increment'
//         })
//     },
// }
</script>

