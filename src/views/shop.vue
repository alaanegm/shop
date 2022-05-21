<template>
  <div class="container">
  
     <div class="shop">
      <div class="content">
        <div class="shop-content">
         
           <p>Shop</p> 
          <p class="line"></p>
          <P><svg xmlns="http://www.w3.org/2000/svg" width="20px" height="20px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class=""><path d="M3 9l9-7 9 7v11a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2z"></path><polyline points="9 22 9 12 15 12 15 22"></polyline></svg></P>
          <p class="Ecommerce">Ecommerce</p>
           <p>shop</p>
      </div>
        <div class="setting">
        <button type="button"><svg xmlns="http://www.w3.org/2000/svg" width="14px" height="14px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-settings"><circle cx="12" cy="12" r="3"></circle><path d="M19.4 15a1.65 1.65 0 0 0 .33 1.82l.06.06a2 2 0 0 1 0 2.83 2 2 0 0 1-2.83 0l-.06-.06a1.65 1.65 0 0 0-1.82-.33 1.65 1.65 0 0 0-1 1.51V21a2 2 0 0 1-2 2 2 2 0 0 1-2-2v-.09A1.65 1.65 0 0 0 9 19.4a1.65 1.65 0 0 0-1.82.33l-.06.06a2 2 0 0 1-2.83 0 2 2 0 0 1 0-2.83l.06-.06a1.65 1.65 0 0 0 .33-1.82 1.65 1.65 0 0 0-1.51-1H3a2 2 0 0 1-2-2 2 2 0 0 1 2-2h.09A1.65 1.65 0 0 0 4.6 9a1.65 1.65 0 0 0-.33-1.82l-.06-.06a2 2 0 0 1 0-2.83 2 2 0 0 1 2.83 0l.06.06a1.65 1.65 0 0 0 1.82.33H9a1.65 1.65 0 0 0 1-1.51V3a2 2 0 0 1 2-2 2 2 0 0 1 2 2v.09a1.65 1.65 0 0 0 1 1.51 1.65 1.65 0 0 0 1.82-.33l.06-.06a2 2 0 0 1 2.83 0 2 2 0 0 1 0 2.83l-.06.06a1.65 1.65 0 0 0-.33 1.82V9a1.65 1.65 0 0 0 1.51 1H21a2 2 0 0 1 2 2 2 2 0 0 1-2 2h-.09a1.65 1.65 0 0 0-1.51 1z"></path></svg></button>
          <div class="dropdown-button">
            <ul>
           <li><a href="#"  target="_self"><svg xmlns="http://www.w3.org/2000/svg" width="16px" height="16px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-check-square"><polyline points="9 11 12 14 22 4"></polyline><path d="M21 12v7a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V5a2 2 0 0 1 2-2h11"></path></svg><span>Todo</span></a></li>
          <li><a href="#" class="dropdown-item"  target="_self"><svg xmlns="http://www.w3.org/2000/svg" width="16px" height="16px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-message-square"><path d="M21 15a2 2 0 0 1-2 2H7l-4 4V5a2 2 0 0 1 2-2h14a2 2 0 0 1 2 2z"></path></svg><span>Chat</span></a></li>
          <li><a href="#" class="dropdown-item"  target="_self"><svg xmlns="http://www.w3.org/2000/svg" width="16px" height="16px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-mail"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"></path><polyline points="22,6 12,13 2,6"></polyline></svg><span>Email</span></a></li>
        <li><a href="#" class="dropdown-item"  target="_self"><svg xmlns="http://www.w3.org/2000/svg" width="16px" height="16px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-calendar"><rect x="3" y="4" width="18" height="18" rx="2" ry="2"></rect><line x1="16" y1="2" x2="16" y2="6"></line><line x1="8" y1="2" x2="8" y2="6"></line><line x1="3" y1="10" x2="21" y2="10"></line></svg><span>Calendar</span></a></li>
            </ul> 
          </div>
      </div>
      </div>
     </div>  
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss">
  .container{
    margin: 0;
    margin-top: 2.5rem;
    margin-left: 285px;
  // background-color:red;
    position: relative;
    width: calc(100% - 4rem - 247px);
    height:100px;
    font-family: 'Segoe UI', Tahoma, sans-serif;
    transition: all .3s ease;
     .shop{
     padding: 0.8rem 1rem;
     //background-color:blue;
     font-family: 'Segoe UI', Tahoma, sans-serif;
      position: relative;
      width:100%; 
      //overflow: hidden;
      display:flex;
      align-items: center;
  .content{
   position: relative;
   width: 100%;
   display:flex;
   align-items:center;
   justify-content: space-between;
    //margin-bottom: 1.5rem;
  .shop-content {
   width: 60%;
   overflow: hidden;
//height:60px;
   display:flex;
   align-items:center;
    margin-left:-1rem;
 .line{
     height:30px;
     border-left:1px solid #7267f094;
   }
   p:first-child{
     font-size: 1.714rem;
      color:#636363;
      padding:0 14px 0 0 ;
      font-weight: 500;
      padding-right: 1rem!important;

   }
   p{
     font-size: 1rem;
      color: #7367f0;
      padding:0 14px 0 0 ;
      background-color: transparent;
   }
   p:nth-of-type(4)::before{
    content:"  ";
    width:15px;
    height:12px;
    margin-right: 0.6rem;
    background-image: url("../assets/downloadarrow.png");
    background-repeat:no-repeat;
    background-position:100%;
    background-size: 17px;
    color: #6e6b7b;
    display:inline-block;
   }
  
    p:last-child::before{
    content:"  ";
    width:15px;
    height:12px;
    margin-right: 0.6rem;
    background-image: url("../assets/downloadarrow.png");
    background-repeat:no-repeat;
    background-position:100%;
    background-size: 17px;
    color: #6e6b7b;
    display:inline-block;
    //font-size: 1.3rem;
   }
   p:last-child{
      color:#636363e3;
      font-size: 1rem;
   }
    
  }///end shop
  
  .setting{
      position: relative;
   // margin-right:0.9rem;
    button{
      // position: relative;
      background-color:#7367f0;
      padding:0.8rem;
      border-radius: 10px;
      border: none;
      svg{
        color:#fff;
      }
    }
    ///////////////////////////
     .dropdown-button {
      min-height: 172px;
      position: absolute;
      min-width: 10rem; 
      font-size: 1rem;
    color: #6e6b7b;
    padding: 0.65rem 1.28rem;
    display:block;
    box-shadow: 0 5px 25px rgb(34 41 47 / 10%);
    background-color:#fff;
    z-index: 1111;
     top: 50px;
     right:-2px;
    border-radius: 0.358rem;
     display: none !important;
   ul{
  position: absolute;
  li{
      a{
          color: #6e6b7b;
          text-decoration: none;
          svg{
               margin-right: 0.5rem;
          }
      }
      margin:15px 15px 0 0;
  }
  
   }
 
}
  }
    }
    
}
  }
 @media screen and (max-width:950px) {
   .container{
     width:96%;
     margin-left:25px;
   }
 }
@media screen and (max-width:700px) {
   .shop-content{
     .hide
     {
         display:none;
     }
     
   }
 }
</style>
