<template>
 <div class="header">
   <navbar  />
 </div>

 <div>
   <shop />
 </div>
 <div>
   <products />
 </div>
 <div>
   <footerPage />
 </div>
 <div>
<!-- <sidbar :mode="mode" @changeColor="$emit('changeColor')"/> -->
 </div>
</template>

<script>
import navbar from '@/views/navbar.vue'
import shop from '@/views/shop.vue'
import products from '@/views/products.vue'
import footerPage from '@/components/footerPage.vue'
import sidbar from '@/components/sidbar.vue'
export default {
  name: 'HelloWorld',
  components:{
    navbar,shop,products,footerPage,sidbar
  },
  props:['mode'],
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style  >
.header{
    position: relative;
    width:100%; 
    height:2.1rem;
    overflow: hidden;
      display:flex;
     justify-content: center;
     align-items:center;
      z-index:1;
      /* background:red; */
}
.dark{
 background-color: #283046;
 color: #b4b7bd;
}
</style>

