<template>
<a @click="toggleSidbar()" data-v-e55d78e2="" href="#" target="_self" class="customizer-toggle"><svg data-v-e55d78e2="" xmlns="http://www.w3.org/2000/svg" width="15px" height="15px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="spinner feather feather-settings"><circle data-v-e55d78e2="" cx="12" cy="12" r="3"></circle><path data-v-e55d78e2="" d="M19.4 15a1.65 1.65 0 0 0 .33 1.82l.06.06a2 2 0 0 1 0 2.83 2 2 0 0 1-2.83 0l-.06-.06a1.65 1.65 0 0 0-1.82-.33 1.65 1.65 0 0 0-1 1.51V21a2 2 0 0 1-2 2 2 2 0 0 1-2-2v-.09A1.65 1.65 0 0 0 9 19.4a1.65 1.65 0 0 0-1.82.33l-.06.06a2 2 0 0 1-2.83 0 2 2 0 0 1 0-2.83l.06-.06a1.65 1.65 0 0 0 .33-1.82 1.65 1.65 0 0 0-1.51-1H3a2 2 0 0 1-2-2 2 2 0 0 1 2-2h.09A1.65 1.65 0 0 0 4.6 9a1.65 1.65 0 0 0-.33-1.82l-.06-.06a2 2 0 0 1 0-2.83 2 2 0 0 1 2.83 0l.06.06a1.65 1.65 0 0 0 1.82.33H9a1.65 1.65 0 0 0 1-1.51V3a2 2 0 0 1 2-2 2 2 0 0 1 2 2v.09a1.65 1.65 0 0 0 1 1.51 1.65 1.65 0 0 0 1.82-.33l.06-.06a2 2 0 0 1 2.83 0 2 2 0 0 1 0 2.83l-.06.06a1.65 1.65 0 0 0-.33 1.82V9a1.65 1.65 0 0 0 1.51 1H21a2 2 0 0 1 2 2 2 2 0 0 1-2 2h-.09a1.65 1.65 0 0 0-1.51 1z"></path></svg></a>
  <div class="sidbar"  v-if="toggle" >
      
     <div class="sidbar-logo">
     <div style="width:95%;">
       <h4> Theme Customizer </h4>
       <span>Customize &amp; Preview in Real Time</span>
     </div>
     <div @click="toggleSidbar()">
         <svg data-v-e55d78e2="" xmlns="http://www.w3.org/2000/svg" width="18px" height="18px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="cursor-pointer feather feather-x"><line data-v-e55d78e2="" x1="18" y1="6" x2="6" y2="18"></line><line data-v-e55d78e2="" x1="6" y1="6" x2="18" y2="18"></line></svg>
     </div>
     </div>
     <div class="sidbar-section">
      
       <div class="block1">
            <p>Skin</p>
           <ul>
             <li><label class="labal">Light
             <input type="radio" checked name="radio" @change="changeColor" value="light" v-model="change">
             <span class="checkmark"></span>
             </label></li>
             <li><label class="labal">Bordered
             <input type="radio"  name="radio" @change="changeColor" value="light" v-model="change">
             <span class="checkmark"></span>
             </label></li>
             <li ><label class="labal">Dark
             <input type="radio"  name="radio" @change="changeColor" value="dark" v-model="change">
             <span class="checkmark"></span>
             </label></li>
             <li><label class="labal">Semi Dark
             <input type="radio"  name="radio" @change="changeColor" value="dark" v-model="change">
             <span class="checkmark"></span>
             </label></li>
           </ul>
       </div>
        <div class="block2">
            <p>Content Width</p>
           <ul>
             <li><label class="labal">Full Width
             <input type="radio" checked name="box">
             <span class="checkmark"></span>
             </label></li>
             <li><label class="labal">Box
             <input type="radio"  name="box">
             <span class="checkmark"></span>
             </label></li>
           </ul>
       </div>
       <div class="block3">
            <p>RTL</p>
            <label class="switch">
            <input type="checkbox">
           <span class="slider round"></span>
           </label>
       </div>
       <div class="block4">
          <p>Router Transition</p>
          <div class="select">
             
              <select class="my_class">
              <option value="Zoom Fade"  selected class="option1">Zoom Fade</option>
               <option value="Fade">Fade</option>
               <option value="Fade Bottom">Fade Bottom</option>
                <option value="Slide Fade">Slide Fade</option>
                 <option value="Zoom out">Zoom out</option>
                 <option value=" None">None</option>
               </select>
         </div>
       </div>
     </div >
     <div class="sidbar-section2">
          <div class="block1">
            <p>Menu Layout</p>
            <ul>
             <li><label class="labal">Full Width
             <input type="radio1" checked name="box">
             <span class="checkmark"></span>
             </label></li>
             <li><label class="labal">Box
             <input type="radio1"  name="box">
             <span class="checkmark"></span>
             </label></li>
           </ul>
       </div>
        <div class="block2">
            <p>Menu Collapsed</p>
            <label class="switch">
            <input type="checkbox">
           <span class="slider round"></span>
           </label>
       </div>
        <div class="block2">
            <p>Menu Hidden</p>
            <label class="switch">
            <input type="checkbox" @change="menuHidden">
           <span class="slider round"></span>
           </label>
       </div>
     </div>
     <div class="sidbar-section3">
       <p>Navbar Color</p>
      <div class="block1">
        <div  class="all" v-for="item in arrColors" :key="item.id" :style="{background: item.color}" @click="changeNavColor(item.id)"></div>
 
      </div>
     </div>
     <div class="section-footer">
          <div class="block1">
            <p>Footer Type</p>
           <ul>
             <li><label class="labal">sticky
             <input type="radio" checked name="radio2" value="sticky" v-model="selected" @change="footerchange">
             <span class="checkmark"></span>
             </label></li>
             <li><label class="labal">static
             <input type="radio"  name="radio2" value="static" v-model="selected" @change="footerchange">
             <span class="checkmark"></span>
             </label></li>
             <li @click="changeColor"><label class="labal">Hidden
             <input type="radio"  name="radio2" value="Hidden" v-model="selected" @change="footerchange">
             <span class="checkmark"></span>
             </label></li>
           </ul>
       </div>
     </div>
  </div>
  
</template>

<script>
export default {
  props:['mode'],
data(){
  return{
    change:"",
    selected:"static",
    show:true,
    toggle:false,
    danger:false,
    theme:" ",
    arrColors:[{color:"#fff",id:1,theme:"white"},{color:"#7367f0",id:2 ,theme:"danger"},{color:"#82868b",id:3,theme:"green"},
    {color:"#28c76f",id:4,theme:"gray"},{color:"#ea5455",id:5,theme:"orange"},{color:"#ff9f43",id:6,theme:"info"},{color:"#00cfe8",id:7,theme:"burble"},{color:"#1e1e1e",id:8,theme:"black"},]
   
  }
 
},
methods:{
  toggleSidbar(){
     this.toggle=!this.toggle
  },
  changeColor(){
  if(this.change=="dark"){
     this.$emit("changeColor",true);
  }
  else  this.$emit("changeColor",false);
     
  },
  changeNavColor(id){
      console.log("this is id "+id)
        let found=this.arrColors.find((item)=>{  
              return item.id === id   });
              this.theme=found?found.theme:" "
              //console.log("arr: "+this.theme)
              this.$emit("changeNavColor",this.theme );
              return this.theme
  },
  menuHidden(){
       this.$emit("menuHidden",this.show);
       this.show=!this.show
  },
  footerchange(){
      if(this.selected=="Hidden"){
         this.$emit("footerchange","Hidden");
      }
      else if(this.selected=="sticky"){
        this.$emit("footerchange","fixed");
      }
      else{
        this.$emit("footerchange","static");
      }
  }


}
}
</script>

<style lang="scss">

.sidbar{
   
   box-shadow: 0 15px 30px 0 rgb(34 41 47 / 11%), 0 5px 15px 0 rgb(34 41 47 / 8%);
   right:0;
   border-left: 1px solid rgba(34,41,47,.05);
   padding: 0;
    background-color: #fff;
    width: 400px;
    z-index: 1051;
    position: fixed;
    top: 0;
    bottom: 0;
    height: 100%;
    //display:none;
   font-family: 'Segoe UI', Tahoma, sans-serif;
   letter-spacing: 1;
   overflow-y: scroll;
   overflow-x: hidden;
    .sidbar-logo{
        width:100%;
        display:flex;
        align-items: center;
        justify-content:center;
        padding: 1.5rem;
        border-bottom: 1px solid #ebe9f1;
        
        h4{
            text-transform: uppercase;
            font-weight: 500;
            line-height: 1.2;
            color: #5e5873;
            margin:0;
            margin-bottom: 5px;
        }
        span{
            font-size: .757rem;
            font-weight: 400;
            color: #898792;
        }
    }
    .sidbar-section{
           padding: 1.5rem;
           border-bottom: 1px solid rgb(235, 233, 241);
       .block1{
           ul{
               display: flex;
               justify-content:space-between;
               align-items: center;
               li{

               }
           }
        }
         .block2{
           ul{
               display: flex;
               justify-content:space-between;
               align-items: center;
               width:50%;
               li{
                  
               }
           }
        } 
        .block3{
    width:100%;
    display:flex;
    justify-content:space-between;
    align-items: center;

        }
      .block4 {
        display:flex;
        justify-content:space-between;
        align-items: center;
        p{
            color: #898792;
          font-weight: 400;
        }
      }
    }
    .sidbar-section2{
      padding: 1.5rem;
      border-bottom: 1px solid rgb(235, 233, 241);
        .block1{
          ul{
               display: flex;
               justify-content:space-between;
               align-items: center;
               width:50%;
           }
        }
       .block2{
          width:100%;
         display:flex;
        justify-content:space-between;
        align-items: center;
       } 
 
    }
     .sidbar-section3{
        padding: 1.5rem;
         border-bottom: 1px solid rgb(235, 233, 241);
       .block1{
         width:100%;
         display:flex;
        justify-content:space-between;
        align-items: center;
        .all{
          width:30px;
          height:30px;
          background:#fff;
          border-radius: 5px;
          border: 1px solid rgba(212, 203, 203, 0.76);
        }
       }
     }
     .section-footer{
        padding: 1.5rem;
         border-bottom: 1px solid rgb(235, 233, 241);
           .block1{
           ul{
               width:70%;
               display: flex;
               justify-content:space-between;
               align-items: center;
           }
        }
     }
      .labal {
  color:#625f6e;
  display: block;
  position: relative;
  padding-left: 1.7rem;
  margin-bottom: 12px;
  cursor: pointer;
  font-size: 14px;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}
.labal input {
  position: absolute;
  opacity: 0;
  cursor: pointer;
}

.checkmark {
  position: absolute;
  top: 0;
  left: 0;
  height: 20px;
  width: 20px;
  border:1px solid #625f6e59;
  border-radius: 50%;
}
.labal:hover input ~ .checkmark {
  background-color: #7367f0;
}
.labal input:checked ~ .checkmark {
  background-color: #7367f0;
}
    .switch {
  position: relative;
  display: inline-block;
  width: 45px;
  height: 25px;
}

.switch input { 
  opacity: 0;
  width: 0;
  height: 0;
}

.slider {
  position: absolute;
  cursor: pointer;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: #ccc;
  -webkit-transition: .4s;
  transition: .4s;
}

.slider:before {
  position: absolute;
  content: "";
  height: 15px;
  width: 15px;
  left:2px;
  bottom: 5px;
  
  background-color: #fff;
  -webkit-transition: .4s;
  transition: .4s;
}

input:checked + .slider {
  background-color: #7367f0;
}

input:focus + .slider {
  box-shadow: 0 0 1px #2196F3;
}

input:checked + .slider:before {
  -webkit-transform: translateX(26px);
  -ms-transform: translateX(26px);
  transform: translateX(26px);
}

.slider.round {
  border-radius: 34px;
}

.slider.round:before {
  border-radius: 50%;
}
}

.my_class{
  text-align:left;
  padding:  10px 20px;
  width:180px;
  color: #6e6b7b;
  border: 1px solid #d8d6de;
  border-radius: 0.357rem;
  background-color: #fff;
  
  &:focus{
    outline:0;
  }
}
 .customizer-toggle{
    display:flex;
    align-items: center;
    justify-content:center;
    box-shadow: -3px 0 8px rgb(34 41 47 / 10%);
    border-top-left-radius: 6px;
    border-bottom-left-radius: 6px;
    right:0;
    background: #7367f0;
    text-align: center;
    cursor: pointer;
    color: #fff!important;
    display: block;
    position: fixed;
    top: 50%;
    width: 38px;
    height: 38px;
    line-height: 40px;
    }
    .danger{
      background-color:#7367f0;
    }
</style>