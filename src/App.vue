<template>
  <div id="app">
  </div>
</template>

<script>
import { useFetch } from 'rexos'
export default {
  name: 'App',
    methods:{
      getData(){
          useFetch('https://api.qq.jsososo.com/songlist?id=2429907335')
         .then(res => {
             console.log(res)
         }).catch(error =>{
             console.log(error)
            })

      }
    },
    created() {
      this.getData()
    }

}
</script>


