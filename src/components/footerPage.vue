  <template>   
 <footer  :class="footerShow" >
   
   <div class="footer_content">
    <p><span> COPYRIGHT © 2022
    <a href="#">Pixinvent</a><span>, All rights Reserved</span></span></p>
  <p><span>Hand-crafted &amp; Made with <svg xmlns="http://www.w3.org/2000/svg" width="21px" height="21px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="text-danger stroke-current feather feather-heart"><path d="M20.84 4.61a5.5 5.5 0 0 0-7.78 0L12 5.67l-1.06-1.06a5.5 5.5 0 0 0-7.78 7.78l1.06 1.06L12 21.23l7.78-7.78 1.06-1.06a5.5 5.5 0 0 0 0-7.78z"></path></svg></span></p>
  </div> 
   <button class="btn">Buy Now</button>
    <button  class="top" @click=" scrollToTop">&#8593;</button>
 </footer>
  
</template>

<script>
export default {
 data(){
    return{
         toggle:true
    }
    
 },
 props:['footerShow'],
//   mounted() {
//       window.addEventListener('scroll',this.handleScroll);
//     },
methods:{
    scrollToTop() {
    window.scrollTo(0,0);
  },
    onScroll (e){
      if (typeof window === 'undefined')   
      return
      const top = window.pageYOffset || e.target.scrollTop || 0
      this.toggle = top > 20
      console.log(top)
      },
}
}
</script>

<style lang="scss">
.Hidden{
  display:none;
}
.fixed{
  position: fixed;
  bottom:0;
  z-index: 111;
  background:#fff;
 
}
.static{
   position: relative;
}
footer{
  // background:black;
   position:relative;
   font-size:0.9rem;
    width: calc(100% - 4rem - 260px);
   color: #6e6b7bcc;
    padding: 0.8rem 0;
    margin: 1.3rem 2rem 0;
    min-height: 3.35rem;
     display:flex;
     align-items: center;
    margin-left: 285px;
   font-family: 'Segoe UI', Tahoma, sans-serif;
     .footer_content{
     //background:red;
  display:flex;
  justify-content:space-between;
   width:100%;
    a{
       
      color:#7367f0;
      text-decoration:none;
    }
    svg{
      margin-left: 0.5rem;
      height: 1.51rem;
    width: 1.51rem;
    font-size: 1.51rem;
    color: #ea5455;
    }
  }
  button{
     display: inline-block;
     text-align: center;
      position:fixed;
     background:#ea5454;
     color:#fff;
     padding: 0.786rem 1.5rem;
      border-radius: 0.358rem;
      border: 1px solid transparent;
     right: 79px;
     bottom: 5%;
    z-index: 1031;
    font-size: 1rem;
    line-height: 1;
    font-weight: 500;
   
    transition: all .15s ease-in-out;
   
  }
  .btn{
    box-shadow: 0 1px 20px 1px #ea5455!important;
  }
  button:hover{
       box-shadow: none;
        border:#ea5454;
  }
  .top{
      display: inline-block;
     text-align: center;
      position:fixed;
    border-color: #7367f0;
    background-color: #7367f0;
     color:#fff;
    padding: 0.715rem 0.936rem;
     border-radius: 0.358rem;
     right: 30px;
    bottom: 5%;
    z-index: 99;
    //opacity: 0;
    font-size: 1.1rem;
    line-height: 1;
    font-weight: 500;
    box-shadow: 0 8px 25px -8px #ea5455;
    transition: all .15s ease-in-out;
  }
}
@media screen and (max-width:950px) {
  footer{
      width:96%;
     margin-left:25px;
  }
}
</style>