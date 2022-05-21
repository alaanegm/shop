<template>
 <div :class="{dark:mode}">
  <div class="header" >
   <navbar :danger="navColor" @chandeMode="chandeMode" :showSidbar="showSidbar"/>
 </div>

 <div>
   <shop />
 </div>
 <div>
   <products />
 </div>
 <div>
   <footerPage :footerShow="footerShow" />
 </div>
    <sidbar  @changeColor="changeColor" @changeNavColor="changeNavColor" @menuHidden="menuHidden" @footerchange="footerchange"
   ></sidbar>
  <router-view/>
 </div>
</template>
<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import navbar from '@/views/navbar.vue'
import shop from '@/views/shop.vue'
import products from '@/views/products.vue'
import footerPage from '@/components/footerPage.vue'
import sidbar from '@/components/sidbar.vue'
export default {
  name: 'HomeView',
  components: {
    HelloWorld, navbar,shop,products,footerPage,sidbar
  },
  data(){
    return{
         mode:false,
         navColor:"danger1",
         showSidbar:" ",
         footerShow:" "
    }
  },
  methods:{
    changeColor(e){
      this.mode=e
      console.log(e)
    },
    changeNavColor(e){
      this.navColor=e
    },
    chandeMode(prams){
      this.mode=!prams

    },
    menuHidden(e){
      this.showSidbar=!e
    },
    footerchange(e){
      this.footerShow=e
    }
  }
}
</script>
<style lang="scss">
* {
  box-sizing: border-box;
}

body {
 background-color: #f8f8f8;
 font-family: Montserrat,Helvetica,Arial,serif;
    font-size: 1rem;
    font-weight: 400;
    line-height: 1.45;
    color: #6e6b7b;
    margin:0;
}

#app{
  
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  font-family: Montserrat,Helvetica,Arial,serif;
    font-size: 1rem;
    font-weight: 400;
    line-height: 1.45;
    color: #6e6b7b;
}

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

#app .dark{
 background-color: #161d31;
 color: #b4b7bd !important;
  nav,.sidenav{
    background-color: #283046;
   li a,p,span{
      color: #b4b7bd !important;
      svg{
         color: #b4b7bd !important;
      }
   }

  }
  .sidbar{
     background-color: #283046;
     .my_class{
       background-color: #283046;
     }
     .slider{
        background-color: #161d31;
     }
     li ,h4,p,label,span{
       color: #b4b7bd !important;
     }
  }
  .shop{
    p{
      color: #b4b7bd !important;
    }
    .Ecommerce ,svg{
      color:#7367f0 !important;
    }
  }
  .products{
    p{
      color: #b4b7bd !important;
    }
    .myclass{
       background-color: #283046;
    }
    .switch-field label{
     background-color: #283046;
    }
    .switch-field input:checked + label {
    background-color: rgba(226, 225, 238, 0.2);
	   box-shadow: none;
     }
    .checkbox{
      background-color: #283046;
      
       li label, p ,h2{
        color: #b4b7bd !important;
       }
    }
    .cards{
      .card,.cart{
        background-color: #283046;
       
       p,li,a{
       color: #b4b7bd !important;
       }
         .Wishlist{
           background-color: #161d31 !important;
           border-color: transparent;
           color: #fff  !important;
         }
          .cart{
         background: #7367f0;
         color: #fff;
         font-weight: 600;
      }
       
      }
      .cart{
         .Wishlist{
           background-color: #161d31 !important;
           border-color: transparent;
           color: #fff  !important;
         }
        .cart{
         background: #7367f0;
         color: #fff;
         font-weight: 600;
      }
      }
      .example input{
          background-color: #283046;
         color: #b4b7bd !important;
      }
    }
  }
    .fixed{
       background-color: #283046 !important;
    }
  
}
.danger{
  background:#ea5455 !important;
}
.white{
  background:#fff !important;
}
.green{
  background:#28c76f !important;
}
.gray{
  background:#82868b;
}
.orange{
  background:#ff9f43;
}
.info{
  background:#00cfe8;
}
.black{
  background:#1e1e1e;
  li a{
    color:#fff;
  }
}
.burble{
  background:#7367f0;
}
</style>
