<template>
   <section class="products ">
        <div class="filter">
            <div class="content">
         <div class="filter-content">
           <p  class="pargr">Filter</p>
           <p><a  href="#"  @click="openside" class="par_toggle"><svg xmlns="http://www.w3.org/2000/svg" width="21px" height="21px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-menu"><line x1="3" y1="12" x2="21" y2="12"></line><line x1="3" y1="6" x2="21" y2="6"></line><line x1="3" y1="18" x2="21" y2="18"></line></svg></a></p> 
          </div>
        <div class="setting">
         <div>
           <p class="found"> {{arr.length}} Results found </p>
         </div>

     <div>
       <form>
      <div>
      <select  v-model="role" @change="selectFun" class="myclass">
       <option value="Highest">Highest</option>
       <option value="Features" selected>Features</option>
       <option value="Lowtest">Lowtest</option>
      </select>
     </div> 
      <div class="switch-field">
		<input type="radio" id="radio-one" name="switch-one" value="yes" checked @change=" closeCart()"/>
		<label for="radio-one"><svg data-v-15eba8c6="" xmlns="http://www.w3.org/2000/svg" width="18px" height="18px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-grid"><rect data-v-15eba8c6="" x="3" y="3" width="7" height="7"></rect><rect data-v-15eba8c6="" x="14" y="3" width="7" height="7"></rect><rect data-v-15eba8c6="" x="14" y="14" width="7" height="7"></rect><rect data-v-15eba8c6="" x="3" y="14" width="7" height="7"></rect></svg></label>
		<input  type="radio" id="radio-two" name="switch-one" value="no"  @change="opencart()" />
	   	<label  for="radio-two"><svg data-v-15eba8c6="" xmlns="http://www.w3.org/2000/svg" width="18px" height="18px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-list"><line data-v-15eba8c6="" x1="8" y1="6" x2="21" y2="6"></line><line data-v-15eba8c6="" x1="8" y1="12" x2="21" y2="12"></line><line data-v-15eba8c6="" x1="8" y1="18" x2="21" y2="18"></line><line data-v-15eba8c6="" x1="3" y1="6" x2="3.01" y2="6"></line><line data-v-15eba8c6="" x1="3" y1="12" x2="3.01" y2="12"></line><line data-v-15eba8c6="" x1="3" y1="18" x2="3.01" y2="18"></line></svg></label>
	     </div>
      </form>
     </div>
      </div>
   
      </div>
         </div>
    <div class="container1">
       
      <div class="checkbox">
     <ul>
    <li><p>Multi Range</p></li>
   <li><label class="labal">All
  <input type="radio" checked name="radio" v-model="All" 
   @change="displayAll" value="All">
  <span class="checkmark"></span>
   </label></li>
   <li><label class="labal"> &#60;&#61; $10
  <input type="radio"  name="radio"   @click="displayless">
  <span class="checkmark"></span>
   </label></li>
   <li><label class="labal">$10 -$100
  <input type="radio"  name="radio" @change="displayMore">
  <span class="checkmark"></span>
   </label></li>
    <li><label class="labal">$100 - $500
  <input type="radio"  name="radio"  @change="displayMore2">
  <span class="checkmark"></span>
   </label></li>
   <li><label class="labal">&#62;&#61;$500
  <input type="radio"  name="radio"  @change="displayMore3">
  <span class="checkmark"></span>
   </label></li>
    <li><h2>Price Range</h2></li>
    <li><input type="range" min="1" max="100" value="50" class="slider"></li>
    <li><h2>Categories</h2></li>
     <li><label class="labal">Appliances
  <input type="radio"  name="switch-two" value="Appliances"  @change="fun">
  <span class="checkmark"></span>
   </label></li>
    <li><label class="labal">Audio
  <input type="radio" name="switch-two">
  <span class="checkmark"></span>
   </label></li>
    <li><label class="labal">Cameras & Camcorders
  <input type="radio"  name="switch-two">
  <span class="checkmark"></span>
   </label></li>
    <li><label class="labal">Car Electronics & GPS
  <input type="radio"  name="switch-two">
  <span class="checkmark"></span>
   </label></li>
    <li><label class="labal">Cell Phones
  <input type="radio"  name="switch-two">
  <span class="checkmark"></span>
   </label></li>
    <li><label class="labal">Computers & Tablets
  <input type="radio"  name="switch-two">
  <span class="checkmark"></span>
   </label></li>
    <li><label class="labal">Health, Fitness & Beauty
  <input type="radio"  name="switch-two">
  <span class="checkmark"></span>
   </label></li>
    <li><label class="labal">Office & School Supplies
  <input type="radio"  name="switch-two">
  <span class="checkmark"></span>
   </label></li>
   <li><label class="labal">TV & Home Theater
  <input type="radio"  name="switch-two">
  <span class="checkmark"></span>
   </label></li>
   <li><label class="labal">Video Games
  <input type="radio" name="switch-two">
  <span class="checkmark"></span>
   </label></li>
   <li><h2>Brands</h2></li>
   <li><label class="labal">Insignia™
  <input type="radio" name="switch-three">
  <span class="checkmark"></span>
   </label></li>
   <li><label class="labal">Samsung
  <input type="radio" name="switch-three">
  <span class="checkmark"></span>
   </label></li>
   <li><label class="labal">Metra
  <input type="radio"  name="switch-three">
  <span class="checkmark"></span>
   </label></li>
   <li><label class="labal">HP
  <input type="radio"  name="switch-three">
  <span class="checkmark"></span>
   </label></li>
   <li><label class="labal">Apple
  <input type="radio"  name="switch-three">
  <span class="checkmark"></span>
   </label></li>
   <li><label class="labal">GE
  <input type="radio"  name="switch-three">
  <span class="checkmark"></span>
   </label></li>
   <li><label class="labal">Sony
  <input type="radio" name="switch-three">
  <span class="checkmark"></span>
   </label></li>
   <li><label class="labal">Incipio
  <input type="radio" name="switch-three">
  <span class="checkmark"></span>
   </label></li>
   <li><label class="labal">KitchenAid
  <input type="radio"  name="switch-three">
  <span class="checkmark"></span>
   </label></li>
   <li><label class="labal">Whirlpool
  <input type="radio"  name="switch-three">
  <span class="checkmark"></span>
   </label></li>
  <li><h2>Ratings</h2></li>
  <li>
    <svg data-v-0f9303ea="" xmlns="http://www.w3.org/2000/svg" width="17px" height="17px" viewBox="0 0 24 24" fill="#ff9f43" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-star fill-current text-warning"><polygon data-v-0f9303ea="" points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon></svg>
    <svg data-v-0f9303ea="" xmlns="http://www.w3.org/2000/svg" width="17px" height="17px" viewBox="0 0 24 24" fill="#ff9f43" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-star fill-current text-warning"><polygon data-v-0f9303ea="" points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon></svg>
    <svg data-v-0f9303ea="" xmlns="http://www.w3.org/2000/svg" width="17px" height="17px" viewBox="0 0 24 24" fill="#ff9f43" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-star fill-current text-warning"><polygon data-v-0f9303ea="" points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon></svg>
    <svg data-v-0f9303ea="" xmlns="http://www.w3.org/2000/svg" width="17px" height="17px" viewBox="0 0 24 24" fill="#ff9f43" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-star fill-current text-warning"><polygon data-v-0f9303ea="" points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon></svg>
    <svg data-v-0f9303ea="" xmlns="http://www.w3.org/2000/svg" width="17px" height="17px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-star fill-current text-warning"><polygon data-v-0f9303ea="" points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon></svg> <span>&up</span></li>
     <li>
    <svg data-v-0f9303ea="" xmlns="http://www.w3.org/2000/svg" width="17px" height="17px" viewBox="0 0 24 24" fill="#ff9f43" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-star fill-current text-warning"><polygon data-v-0f9303ea="" points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon></svg>
    <svg data-v-0f9303ea="" xmlns="http://www.w3.org/2000/svg" width="17px" height="17px" viewBox="0 0 24 24" fill="#ff9f43" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-star fill-current text-warning"><polygon data-v-0f9303ea="" points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon></svg>
    <svg data-v-0f9303ea="" xmlns="http://www.w3.org/2000/svg" width="17px" height="17px" viewBox="0 0 24 24" fill="#ff9f43" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-star fill-current text-warning"><polygon data-v-0f9303ea="" points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon></svg>
    <svg data-v-0f9303ea="" xmlns="http://www.w3.org/2000/svg" width="17px" height="17px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-star fill-current text-warning"><polygon data-v-0f9303ea="" points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon></svg>
    <svg data-v-0f9303ea="" xmlns="http://www.w3.org/2000/svg" width="17px" height="17px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-star fill-current text-warning"><polygon data-v-0f9303ea="" points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon></svg> <span>&up</span></li>
     <li>
    <svg data-v-0f9303ea="" xmlns="http://www.w3.org/2000/svg" width="17px" height="17px" viewBox="0 0 24 24" fill="#ff9f43" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-star fill-current text-warning"><polygon data-v-0f9303ea="" points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon></svg>
    <svg data-v-0f9303ea="" xmlns="http://www.w3.org/2000/svg" width="17px" height="17px" viewBox="0 0 24 24" fill="#ff9f43" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-star fill-current text-warning"><polygon data-v-0f9303ea="" points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon></svg>
    <svg data-v-0f9303ea="" xmlns="http://www.w3.org/2000/svg" width="17px" height="17px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-star fill-current text-warning"><polygon data-v-0f9303ea="" points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon></svg>
    <svg data-v-0f9303ea="" xmlns="http://www.w3.org/2000/svg" width="17px" height="17px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-star fill-current text-warning"><polygon data-v-0f9303ea="" points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon></svg>
    <svg data-v-0f9303ea="" xmlns="http://www.w3.org/2000/svg" width="17px" height="17px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-star fill-current text-warning"><polygon data-v-0f9303ea="" points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon></svg> <span>&up</span> </li>
     <li>
    <svg data-v-0f9303ea="" xmlns="http://www.w3.org/2000/svg" width="17px" height="17px" viewBox="0 0 24 24" fill="#ff9f43" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-star fill-current text-warning"><polygon data-v-0f9303ea="" points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon></svg>
    <svg data-v-0f9303ea="" xmlns="http://www.w3.org/2000/svg" width="17px" height="17px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-star fill-current text-warning"><polygon data-v-0f9303ea="" points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon></svg>
    <svg data-v-0f9303ea="" xmlns="http://www.w3.org/2000/svg" width="17px" height="17px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-star fill-current text-warning"><polygon data-v-0f9303ea="" points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon></svg>
    <svg data-v-0f9303ea="" xmlns="http://www.w3.org/2000/svg" width="17px" height="17px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-star fill-current text-warning"><polygon data-v-0f9303ea="" points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon></svg>
    <svg data-v-0f9303ea="" xmlns="http://www.w3.org/2000/svg" width="17px" height="17px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-star fill-current text-warning"><polygon data-v-0f9303ea="" points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon></svg> <span>&up</span> </li>
     
     </ul>
       </div>
        <div class="sidenav-overlay" v-if="toggle" >
        <div class="checkbox1" >
     <ul>
    <li><p>Multi Range</p></li>
   <li><label class="labal">All
  <input type="radio" checked name="radio" v-model="All" 
   @change="displayAll" value="All">
  <span class="checkmark"></span>
   </label></li>
   <li><label class="labal"> &#60;&#61; $10
  <input type="radio"  name="radio"   @click="displayless">
  <span class="checkmark"></span>
   </label></li>
   <li><label class="labal">$10 -$100
  <input type="radio"  name="radio" @change="displayMore">
  <span class="checkmark"></span>
   </label></li>
    <li><label class="labal">$100 - $500
  <input type="radio"  name="radio"  @change="displayMore2">
  <span class="checkmark"></span>
   </label></li>
   <li><label class="labal">&#62;&#61;$500
  <input type="radio"  name="radio"  @change="displayMore3">
  <span class="checkmark"></span>
   </label></li>
    <li><h2>Price Range</h2></li>
    <li><input type="range" min="1" max="100" value="50" class="slider"></li>
    <li><h2>Categories</h2></li>
     <li><label class="labal">Appliances
  <input type="radio"  name="radio5" value="Appliances" @change="displayMore3">
  <span class="checkmark"></span>
   </label></li>
    <li><label class="labal">Audio
  <input type="radio" name="radio5">
  <span class="checkmark"></span>
   </label></li>
    <li><label class="labal">Cameras & Camcorders
  <input type="radio"  name="radio5">
  <span class="checkmark"></span>
   </label></li>
    <li><label class="labal">Car Electronics & GPS
  <input type="radio"  name="radio5">
  <span class="checkmark"></span>
   </label></li>
    <li><label class="labal">Cell Phones
  <input type="radio"  name="radio5">
  <span class="checkmark"></span>
   </label></li>
    <li><label class="labal">Computers & Tablets
  <input type="radio"  name="radio5">
  <span class="checkmark"></span>
   </label></li>
    <li><label class="labal">Health, Fitness & Beauty
  <input type="radio"  name="radio5">
  <span class="checkmark"></span>
   </label></li>
    <li><label class="labal">Office & School Supplies
  <input type="radio"  name="radio5">
  <span class="checkmark"></span>
   </label></li>
   <li><label class="labal">TV & Home Theater
  <input type="radio"  name="radio5">
  <span class="checkmark"></span>
   </label></li>
   <li><label class="labal">Video Games
  <input type="radio" name="radio5">
  <span class="checkmark"></span>
   </label></li>
   <li><h2>Brands</h2></li>
   <li><label class="labal">Insignia™
  <input type="radio" name="radio4" v-model="brand" value="Insignia™" @change="selectBrand" > 
  <span class="checkmark"></span>
   </label></li>
   <li><label class="labal">Samsung
  <input type="radio" name="radio4" v-model="brand" value="Samsung" @change="selectBrand">
  <span class="checkmark"></span>
   </label></li>
   <li><label class="labal">Metra
  <input type="radio"  name="radio4" v-model="brand" value="Metra" @change="selectBrand">
  <span class="checkmark"></span>
   </label></li>
   <li><label class="labal">HP
  <input type="radio"  name="radio4" v-model="brand" value="HP" @change="selectBrand">
  <span class="checkmark"></span>
   </label></li>
   <li><label class="labal">Apple
  <input type="radio"  name="radio4" v-model="brand" value="Apple" @change="selectBrand">
  <span class="checkmark"></span>
   </label></li>
   <li><label class="labal">GE
  <input type="radio"  name="radio4" v-model="brand" value="GE" @change="selectBrand">
  <span class="checkmark"></span>
   </label></li>
   <li><label class="labal">Sony
  <input type="radio" name="radio4" v-model="brand" value="Sony" @change="selectBrand">
  <span class="checkmark"></span>
   </label></li>
   <li><label class="labal">Incipio
  <input type="radio" name="radio4" v-model="brand" value="Incipio" @change="selectBrand">
  <span class="checkmark"></span>
   </label></li>
   <li><label class="labal">KitchenAid
  <input type="radio"  name="radio4" v-model="brand" value="KitchenAid" @change="selectBrand">
  <span class="checkmark"></span>
   </label></li>
   <li><label class="labal">Whirlpool
  <input type="radio"  name="radio4" v-model="brand" value="Whirlpool" @change="selectBrand">
  <span class="checkmark"></span>
   </label></li>
  <li><h2>Ratings</h2></li>
  <li>
    <svg data-v-0f9303ea="" xmlns="http://www.w3.org/2000/svg" width="17px" height="17px" viewBox="0 0 24 24" fill="#ff9f43" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-star fill-current text-warning"><polygon data-v-0f9303ea="" points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon></svg>
    <svg data-v-0f9303ea="" xmlns="http://www.w3.org/2000/svg" width="17px" height="17px" viewBox="0 0 24 24" fill="#ff9f43" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-star fill-current text-warning"><polygon data-v-0f9303ea="" points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon></svg>
    <svg data-v-0f9303ea="" xmlns="http://www.w3.org/2000/svg" width="17px" height="17px" viewBox="0 0 24 24" fill="#ff9f43" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-star fill-current text-warning"><polygon data-v-0f9303ea="" points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon></svg>
    <svg data-v-0f9303ea="" xmlns="http://www.w3.org/2000/svg" width="17px" height="17px" viewBox="0 0 24 24" fill="#ff9f43" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-star fill-current text-warning"><polygon data-v-0f9303ea="" points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon></svg>
    <svg data-v-0f9303ea="" xmlns="http://www.w3.org/2000/svg" width="17px" height="17px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-star fill-current text-warning"><polygon data-v-0f9303ea="" points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon></svg> <span>&up</span></li>
     <li>
    <svg data-v-0f9303ea="" xmlns="http://www.w3.org/2000/svg" width="17px" height="17px" viewBox="0 0 24 24" fill="#ff9f43" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-star fill-current text-warning"><polygon data-v-0f9303ea="" points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon></svg>
    <svg data-v-0f9303ea="" xmlns="http://www.w3.org/2000/svg" width="17px" height="17px" viewBox="0 0 24 24" fill="#ff9f43" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-star fill-current text-warning"><polygon data-v-0f9303ea="" points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon></svg>
    <svg data-v-0f9303ea="" xmlns="http://www.w3.org/2000/svg" width="17px" height="17px" viewBox="0 0 24 24" fill="#ff9f43" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-star fill-current text-warning"><polygon data-v-0f9303ea="" points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon></svg>
    <svg data-v-0f9303ea="" xmlns="http://www.w3.org/2000/svg" width="17px" height="17px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-star fill-current text-warning"><polygon data-v-0f9303ea="" points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon></svg>
    <svg data-v-0f9303ea="" xmlns="http://www.w3.org/2000/svg" width="17px" height="17px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-star fill-current text-warning"><polygon data-v-0f9303ea="" points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon></svg> <span>&up</span></li>
     <li>
    <svg data-v-0f9303ea="" xmlns="http://www.w3.org/2000/svg" width="17px" height="17px" viewBox="0 0 24 24" fill="#ff9f43" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-star fill-current text-warning"><polygon data-v-0f9303ea="" points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon></svg>
    <svg data-v-0f9303ea="" xmlns="http://www.w3.org/2000/svg" width="17px" height="17px" viewBox="0 0 24 24" fill="#ff9f43" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-star fill-current text-warning"><polygon data-v-0f9303ea="" points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon></svg>
    <svg data-v-0f9303ea="" xmlns="http://www.w3.org/2000/svg" width="17px" height="17px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-star fill-current text-warning"><polygon data-v-0f9303ea="" points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon></svg>
    <svg data-v-0f9303ea="" xmlns="http://www.w3.org/2000/svg" width="17px" height="17px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-star fill-current text-warning"><polygon data-v-0f9303ea="" points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon></svg>
    <svg data-v-0f9303ea="" xmlns="http://www.w3.org/2000/svg" width="17px" height="17px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-star fill-current text-warning"><polygon data-v-0f9303ea="" points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon></svg> <span>&up</span> </li>
     <li>
    <svg data-v-0f9303ea="" xmlns="http://www.w3.org/2000/svg" width="17px" height="17px" viewBox="0 0 24 24" fill="#ff9f43" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-star fill-current text-warning"><polygon data-v-0f9303ea="" points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon></svg>
    <svg data-v-0f9303ea="" xmlns="http://www.w3.org/2000/svg" width="17px" height="17px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-star fill-current text-warning"><polygon data-v-0f9303ea="" points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon></svg>
    <svg data-v-0f9303ea="" xmlns="http://www.w3.org/2000/svg" width="17px" height="17px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-star fill-current text-warning"><polygon data-v-0f9303ea="" points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon></svg>
    <svg data-v-0f9303ea="" xmlns="http://www.w3.org/2000/svg" width="17px" height="17px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-star fill-current text-warning"><polygon data-v-0f9303ea="" points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon></svg>
    <svg data-v-0f9303ea="" xmlns="http://www.w3.org/2000/svg" width="17px" height="17px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-star fill-current text-warning"><polygon data-v-0f9303ea="" points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon></svg> <span>&up</span> </li>
     
     </ul>
       </div>
       <div class="overlay-side" @click="closeSide">
       </div>
        </div>
       <!--         ---------------------    start cards -->
          <div class="cards">
      <div class="shop-cards">
      <div class="search">
      <form class="example" action="/action_page.php">
      <input type="text" placeholder="Search.." name="search" v-model="search" @keyup="searchFun">
      </form>
      </div>
      
  <div class="card" v-for="product in arr" :key="product.id"  v-bind:style="{display:open}">
   <img alt="Vue logo" :src="product.img"  style="width:100%">
  <div class="card-content">
    <div class="price">
    <div class="price-content" style="padding:1rem;">
      <div class="rating">
        <div> 
        <ul >
          <li v-for="(item, index) in 5" :key="index" ><svg  v-if="index<product.rating" data-v-0f9303ea="" xmlns="http://www.w3.org/2000/svg" width="17px" height="17px" viewBox="0 0 24 24" fill="#ff9f43" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-star fill-current text-warning"><polygon data-v-0f9303ea="" points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon></svg>
          <svg  v-else data-v-0f9303ea="" xmlns="http://www.w3.org/2000/svg" width="17px" height="17px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-star fill-current text-warning"><polygon data-v-0f9303ea="" points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon></svg></li>
      </ul>
      </div>
        <div >
          <ul>
            <li><span class="price1">${{product.price}}</span></li>
          </ul>

        </div>
      </div>
     
    <p class="item-name"><a href="#">{{product.name}}</a></p>
    <p class="discription">{{product.discription}}</p>
     </div>
    <div class="card-button">
    <p class="items-button"> <a href="#" class="Wishlist"><svg data-v-15eba8c6="" xmlns="http://www.w3.org/2000/svg" width="14px" height="14px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="mr-50 feather feather-heart"><path data-v-15eba8c6="" d="M20.84 4.61a5.5 5.5 0 0 0-7.78 0L12 5.67l-1.06-1.06a5.5 5.5 0 0 0-7.78 7.78l1.06 1.06L12 21.23l7.78-7.78 1.06-1.06a5.5 5.5 0 0 0 0-7.78z"></path></svg>
    Wishlist</a>
        <a href="#" class="cart"><svg data-v-15eba8c6="" xmlns="http://www.w3.org/2000/svg" width="14px" height="14px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="mr-50 feather feather-shopping-cart"><circle data-v-15eba8c6="" cx="9" cy="21" r="1"></circle><circle data-v-15eba8c6="" cx="20" cy="21" r="1"></circle><path data-v-15eba8c6="" d="M1 1h4l2.68 13.39a2 2 0 0 0 2 1.61h9.72a2 2 0 0 0 2-1.61L23 6H6"></path></svg>
          View In Cart</a></p>
    </div>
    </div>
  </div>
   </div> 
   	
        <div class="cart" v-for="product in arr" :key="product.id"  v-bind:style="{display:block}">
        <div class="cart-content">
          <div class="block-img">
             <img alt="Vue logo" :src="product.img"  style="width:100%">
        </div>
        <div class="block1">
          <p> <a href="#">{{product.name}}...</a></p>
          <p>   <svg data-v-0f9303ea="" xmlns="http://www.w3.org/2000/svg" width="17px" height="17px" viewBox="0 0 24 24" fill="#ff9f43" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-star fill-current text-warning"><polygon data-v-0f9303ea="" points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon></svg>
                <svg data-v-0f9303ea="" xmlns="http://www.w3.org/2000/svg" width="17px" height="17px" viewBox="0 0 24 24" fill="#ff9f43" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-star fill-current text-warning"><polygon data-v-0f9303ea="" points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon></svg>
                <svg data-v-0f9303ea="" xmlns="http://www.w3.org/2000/svg" width="17px" height="17px" viewBox="0 0 24 24" fill="#ff9f43" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-star fill-current text-warning"><polygon data-v-0f9303ea="" points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon></svg>
                <svg data-v-0f9303ea="" xmlns="http://www.w3.org/2000/svg" width="17px" height="17px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-star fill-current text-warning"><polygon data-v-0f9303ea="" points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon></svg>
                <svg data-v-0f9303ea="" xmlns="http://www.w3.org/2000/svg" width="17px" height="17px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-star fill-current text-warning"><polygon data-v-0f9303ea="" points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon></svg> </p>
          <p class="discription">{{product.discription}}</p>
          
        </div>
        <div class="block2">
              <p style="color:#7367f0; font-size:1.2rem;">  <span >${{product.price}}</span></p>
                <div class="card-button">
               <p> <a href="#" class="Wishlist">Wishlist</a>
            <a href="#" class="cart">View In Cart</a></p>
              </div>
              </div>
        </div>
      </div>
  </div>
 

   </div>
   
      </div>
 
  </section>
</template>

<script>
export default {
  created() {
     this.paginate_total = this.arr.length/this.paginate;
     console.log("paginate_total"+ this.paginate_total)
     console.log(this.arr.length)
   },
data(){
        return{
           toggle:false,
          Appliances:'',
          flag:false,
          role:'Features',
           cardFlag:false,
            products:[{
            "id":1,
            "name": "Apple Watch Series 5",
            "price": 339.99,
            "rating": 4,
            "img": "https://pixinvent.com/demo/vuexy-vuejs-admin-dashboard-template/demo-1/img/1.3b312012.png",
            "discription": "On Retina display that never sleeps, so it’s easy to see the time and other important information, without raising or tapping the display. New location features, from a built-in compass to current elevation, help users better navigate their day, while international emergency calling1 allows customers to call emergency services directly from Apple Watch in over 150 countries, even without iPhone nearby. Apple Watch Series 5 is available in a wider range of materials, including aluminium, stainless steel, ceramic and an all-new titanium.",
            "brand": "apple",
            "available": true,
            "colors": ["red", "purple", "green"]
        },
        {
            "id":2,
            "name": "Apple iPhone 11 (64GB, Black)",
            "price": 669.99,
            "rating": 5,
            "img": "https://pixinvent.com/demo/vuexy-vuejs-admin-dashboard-template/demo-1/img/2.1aba2cea.png",
            "discription": "On Retina display that never sleeps, so it’s easy to see the time and other important information, without raising or tapping the display. New location features, from a built-in compass to current elevation, help users better navigate their day, while international emergency calling1 allows customers to call emergency services directly from Apple Watch in over 150 countries, even without iPhone nearby. Apple Watch Series 5 is available in a wider range of materials, including aluminium, stainless steel, ceramic and an all-new titanium.",
            "brand": "apple",
            "available": true,
            "colors": ["red", "purple", "green"]
        },
        {
            "id":3,
            "name": "Apple iMac 27-inch",
            "price": 999.99,
            "rating": 4,
            "img": "https://pixinvent.com/demo/vuexy-vuejs-admin-dashboard-template/demo-1/img/3.29c766f8.png",
            "discription": "On Retina display that never sleeps, so it’s easy to see the time and other important information, without raising or tapping the display. New location features, from a built-in compass to current elevation, help users better navigate their day, while international emergency calling1 allows customers to call emergency services directly from Apple Watch in over 150 countries, even without iPhone nearby. Apple Watch Series 5 is available in a wider range of materials, including aluminium, stainless steel, ceramic and an all-new titanium.",
            "brand": "apple",
            "available": true,
            "colors": ["red", "purple", "green"]
        },
        {
            "id":4,
            "name": "OneOdio A71 Wired Headphones",
            "price": 49.99,
            "rating": 3,
            "img": "https://pixinvent.com/demo/vuexy-vuejs-admin-dashboard-template/demo-1/img/4.73f34744.png",
            "discription": "On Retina display that never sleeps, so it’s easy to see the time and other important information, without raising or tapping the display. New location features, from a built-in compass to current elevation, help users better navigate their day, while international emergency calling1 allows customers to call emergency services directly from Apple Watch in over 150 countries, even without iPhone nearby. Apple Watch Series 5 is available in a wider range of materials, including aluminium, stainless steel, ceramic and an all-new titanium.",
            "brand": "apple",
            "available": true,
            "colors": ["red", "purple", "green"]
        },
        {
            "id":5,
            "name": "Apple - MacBook Air® (Latest Model) - 13.3 Display - Silver",
            "price": 999.99,
            "rating": 4,
            "img": "https://pixinvent.com/demo/vuexy-vuejs-admin-dashboard-template/demo-1/img/5.c5b188e5.png",
            "discription": "On Retina display that never sleeps, so it’s easy to see the time and other important information, without raising or tapping the display. New location features, from a built-in compass to current elevation, help users better navigate their day, while international emergency calling1 allows customers to call emergency services directly from Apple Watch in over 150 countries, even without iPhone nearby. Apple Watch Series 5 is available in a wider range of materials, including aluminium, stainless steel, ceramic and an all-new titanium.",
            "brand": "apple",
            "available": true,
            "colors": ["red", "purple", "green"]
        },
        {
            "id":6,
            "name": "Switch Pro Controller",
            "price": 429.99,
            "rating": 3,
            "img": "https://pixinvent.com/demo/vuexy-vuejs-admin-dashboard-template/demo-1/img/6.833c8951.png",
            "discription": "On Retina display that never sleeps, so it’s easy to see the time and other important information, without raising or tapping the display. New location features, from a built-in compass to current elevation, help users better navigate their day, while international emergency calling1 allows customers to call emergency services directly from Apple Watch in over 150 countries, even without iPhone nearby. Apple Watch Series 5 is available in a wider range of materials, including aluminium, stainless steel, ceramic and an all-new titanium.",
            "brand": "apple",
            "available": true,
            "colors": ["red", "purple", "green"]
        },
        {
            "id":7,
            "name": "Google - Google Home - White/Slate fabric",
            "price": 129.29,
            "rating": 4,
            "img": "https://pixinvent.com/demo/vuexy-vuejs-admin-dashboard-template/demo-1/img/1.3b312012.png",
            "discription": "On Retina display that never sleeps, so it’s easy to see the time and other important information, without raising or tapping the display. New location features, from a built-in compass to current elevation, help users better navigate their day, while international emergency calling1 allows customers to call emergency services directly from Apple Watch in over 150 countries, even without iPhone nearby. Apple Watch Series 5 is available in a wider range of materials, including aluminium, stainless steel, ceramic and an all-new titanium.",
            "brand": "google",
            "available": true,
            "colors": ["red", "purple", "green"]
        },
        {
            "id":8,
            "name": "Sony 4K Ultra HD LED TV",
            "price": 7999.99,
            "rating": 5,
            "img": "https://pixinvent.com/demo/vuexy-vuejs-admin-dashboard-template/demo-1/img/8.c170e8ca.png",
            "discription": "On Retina display that never sleeps, so it’s easy to see the time and other important information, without raising or tapping the display. New location features, from a built-in compass to current elevation, help users better navigate their day, while international emergency calling1 allows customers to call emergency services directly from Apple Watch in over 150 countries, even without iPhone nearby. Apple Watch Series 5 is available in a wider range of materials, including aluminium, stainless steel, ceramic and an all-new titanium.",
            "brand": "apple",
            "available": true,
            "colors": ["red", "purple", "green"]
        },
        {
            "id":9,
            "name": "OnePlus 7 Pro",
            "price": 14.99,
            "rating": 4,
            "img": "https://pixinvent.com/demo/vuexy-vuejs-admin-dashboard-template/demo-1/img/9.3170c803.png",
            "discription": "On Retina display that never sleeps, so it’s easy to see the time and other important information, without raising or tapping the display. New location features, from a built-in compass to current elevation, help users better navigate their day, while international emergency calling1 allows customers to call emergency services directly from Apple Watch in over 150 countries, even without iPhone nearby. Apple Watch Series 5 is available in a wider range of materials, including aluminium, stainless steel, ceramic and an all-new titanium.",
            "brand": "Philips",
            "available": true,
            "colors": ["red", "purple", "green"]
        },
        {
            "id":10,
            "name": "Logitech K380 Wireless Keyboard",
            "price": 81.99,
            "rating": 4,
            "img": "https://pixinvent.com/demo/vuexy-vuejs-admin-dashboard-template/demo-1/img/10.a197f12f.png",
            "discription": "On Retina display that never sleeps, so it’s easy to see the time and other important information, without raising or tapping the display. New location features, from a built-in compass to current elevation, help users better navigate their day, while international emergency calling1 allows customers to call emergency services directly from Apple Watch in over 150 countries, even without iPhone nearby. Apple Watch Series 5 is available in a wider range of materials, including aluminium, stainless steel, ceramic and an all-new titanium.",
            "brand": "Logitech",
            "available": true,
            "colors": ["red", "purple", "green"]
        },
        {
            "id":11,
            "name": "Nike Air Max",
            "price": 81.99,
            "rating": 5,
            "img": "https://pixinvent.com/demo/vuexy-vuejs-admin-dashboard-template/demo-1/img/11.196910d4.png",
            "discription": "On Retina display that never sleeps, so it’s easy to see the time and other important information, without raising or tapping the display. New location features, from a built-in compass to current elevation, help users better navigate their day, while international emergency calling1 allows customers to call emergency services directly from Apple Watch in over 150 countries, even without iPhone nearby.  is available in a wider range of materials, including aluminium, stainless steel, ceramic and an all-new titanium.",
            "brand": "Nike",
            "available": true,
            "colors": ["red", "purple", "green"]
        },
        {
            "id":12,
            "name": "New Apple iPad Pro",
            "price": 799.99,
            "rating": 4,
            "img": "https://pixinvent.com/demo/vuexy-vuejs-admin-dashboard-template/demo-1/img/12.87084176.png",
            "discription": "On Retina display that never sleeps, so it’s easy to see the time and other important information, without raising or tapping the display. New location features, from a built-in compass to current elevation, help users better navigate their day, while international emergency calling1 allows customers to call emergency services directly from Apple Watch in over 150 countries, even without iPhone nearby.  is available in a wider range of materials, including aluminium, stainless steel, ceramic and an all-new titanium.",
            "brand": "apple",
            "available": true,
            "colors": ["red", "purple", "green"]
        },
        {
            "id":13,
            "name": "Vankyo leisure 3 mini projector",
            "price": 99.99,
            "rating": 2,
            "img": "https://pixinvent.com/demo/vuexy-vuejs-admin-dashboard-template/demo-1/img/13.e7c28d6c.png",
            "discription": "On Retina display that never sleeps, so it’s easy to see the time and other important information, without raising or tapping the display. New location features, from a built-in compass to current elevation, help users better navigate their day, while international emergency calling1 allows customers to call emergency services directly from Apple Watch in over 150 countries, even without iPhone nearby.  is available in a wider range of materials, including aluminium, stainless steel, ceramic and an all-new titanium.",
            "brand": "Vankyo Store",
            "available": true,
            "colors": ["red", "purple", "green"]
        },
        {
            "id":14,
            "name": "Wireless Charger 5W Max",
            "price": 10.83,
            "rating": 4,
            "img": "https://pixinvent.com/demo/vuexy-vuejs-admin-dashboard-template/demo-1/img/14.df784ed6.png",
            "discription": "On Retina display that never sleeps, so it’s easy to see the time and other important information, without raising or tapping the display. New location features, from a built-in compass to current elevation, help users better navigate their day, while international emergency calling1 allows customers to call emergency services directly from Apple Watch in over 150 countries, even without iPhone nearby.  is available in a wider range of materials, including aluminium, stainless steel, ceramic and an all-new titanium.",
            "brand": "3M",
            "available": true,
            "colors": ["red", "purple", "green"]
        },
        {
            "id":15,
            "name": "Laptop Bag",
            "price": 29.99,
            "rating": 5,
            "img": "https://pixinvent.com/demo/vuexy-vuejs-admin-dashboard-template/demo-1/img/15.2b721276.png",
            "discription": "On Retina display that never sleeps, so it’s easy to see the time and other important information, without raising or tapping the display. New location features, from a built-in compass to current elevation, help users better navigate their day, while international emergency calling1 allows customers to call emergency services directly from Apple Watch in over 150 countries, even without iPhone nearby.  is available in a wider range of materials, including aluminium, stainless steel, ceramic and an all-new titanium.",
            "brand": "TAS",
            "available": true,
            "colors": ["red", "purple", "green"]
        },
        {
            "id":16,
            "name": "Adidas Mens Tech Response Shoes",
            "price": 54.59,
            "rating": 5,
            "img": "https://pixinvent.com/demo/vuexy-vuejs-admin-dashboard-template/demo-1/img/16.a9b3f7ab.png",
            "discription": "On Retina display that never sleeps, so it’s easy to see the time and other important information, without raising or tapping the display. New location features, from a built-in compass to current elevation, help users better navigate their day, while international emergency calling1 allows customers to call emergency services directly from Apple Watch in over 150 countries, even without iPhone nearby.  is available in a wider range of materials, including aluminium, stainless steel, ceramic and an all-new titanium.",
            "brand": "Adidas",
            "available": true,
            "colors": ["red", "purple", "green"]
        },
        {
            "id":17,
            "name": "Oculus Quest All-in-one VR",
            "price": 645,
            "rating": 1,
            "img": "https://pixinvent.com/demo/vuexy-vuejs-admin-dashboard-template/demo-1/img/18.fac01044.png",
            "discription": "On Retina display that never sleeps, so it’s easy to see the time and other important information, without raising or tapping the display. New location features, from a built-in compass to current elevation, help users better navigate their day, while international emergency calling1 allows customers to call emergency services directly from Apple Watch in over 150 countries, even without iPhone nearby.  is available in a wider range of materials, including aluminium, stainless steel, ceramic and an all-new titanium.",
            "brand": "Oculus",
            "available": true,
            "colors": ["red", "purple", "green"]
        },
        {
            "id":18,
            "name": "Handbags for Women Large Designer bag",
            "price": 39.99,
            "rating": 4,
            "img": "https://pixinvent.com/demo/vuexy-vuejs-admin-dashboard-template/demo-1/img/17.024d4a22.png",
            "discription": "On Retina display that never sleeps, so it’s easy to see the time and other important information, without raising or tapping the display. New location features, from a built-in compass to current elevation, help users better navigate their day, while international emergency calling1 allows customers to call emergency services directly from Apple Watch in over 150 countries, even without iPhone nearby.  is available in a wider range of materials, including aluminium, stainless steel, ceramic and an all-new titanium.",
            "brand": "Hobo",
            "available": true,
            "colors": ["red", "purple", "green"]
        },
        {
            "id":19,
            "name": "Giotto 32oz Leakproof BPA Free Drinking Water",
            "price": 16.99,
            "rating": 4,
            "img": "https://pixinvent.com/demo/vuexy-vuejs-admin-dashboard-template/demo-1/img/19.1c1f4cf1.png",
            "discription": "On Retina display that never sleeps, so it’s easy to see the time and other important information, without raising or tapping the display. New location features, from a built-in compass to current elevation, help users better navigate their day, while international emergency calling1 allows customers to call emergency services directly from Apple Watch in over 150 countries, even without iPhone nearby.  is available in a wider range of materials, including aluminium, stainless steel, ceramic and an all-new titanium.",
            "brand": "3M",
            "available": true,
            "colors": ["red", "purple", "green"]
        },
        {
            "id":20,
            "name": "PlayStation 4 Console",
            "price": 339.95,
            "rating": 4,
            "img": "https://pixinvent.com/demo/vuexy-vuejs-admin-dashboard-template/demo-1/img/20.ad629602.png",
            "discription": "On Retina display that never sleeps, so it’s easy to see the time and other important information, without raising or tapping the display. New location features, from a built-in compass to current elevation, help users better navigate their day, while international emergency calling1 allows customers to call emergency services directly from Apple Watch in over 150 countries, even without iPhone nearby.  is available in a wider range of materials, including aluminium, stainless steel, ceramic and an all-new titanium.",
            "brand": "Sony",
            "available": true,
            "colors": ["red", "purple", "green"]
        },
        {
            "id":21,
            "name": "Bugani M90 Portable Bluetooth Speaker",
            "price": 56,
            "rating": 4,
            "img": "https://pixinvent.com/demo/vuexy-vuejs-admin-dashboard-template/demo-1/img/21.940a62ff.png",
            "discription": "On Retina display that never sleeps, so it’s easy to see the time and other important information, without raising or tapping the display. New location features, from a built-in compass to current elevation, help users better navigate their day, while international emergency calling1 allows customers to call emergency services directly from Apple Watch in over 150 countries, even without iPhone nearby.  is available in a wider range of materials, including aluminium, stainless steel, ceramic and an all-new titanium.",
            "brand": "Bugani",
            "available": true,
            "colors": ["red", "purple", "green"]
        },
        {
            "id":22,
            "name": "Toshiba Canvio Advance 2TB Portable External Hard Drive",
            "price": 69.99,
            "rating": 4,
            "img": "https://pixinvent.com/demo/vuexy-vuejs-admin-dashboard-template/demo-1/img/23.ec286c40.png",
            "discription": "On Retina display that never sleeps, so it’s easy to see the time and other important information, without raising or tapping the display. New location features, from a built-in compass to current elevation, help users better navigate their day, while international emergency calling1 allows customers to call emergency services directly from Apple Watch in over 150 countries, even without iPhone nearby.  is available in a wider range of materials, including aluminium, stainless steel, ceramic and an all-new titanium.",
            "brand": "Toshiba",
            "available": true,
            "colors": ["red", "purple", "green"]
        },
        {
            "id":23,
            "name": "Tile Pro - High Performance Bluetooth Tracker",
            "price": 29.99,
            "rating": 3,
            "img": "https://pixinvent.com/demo/vuexy-vuejs-admin-dashboard-template/demo-1/img/22.450e8e03.png",
            "discription": "On Retina display that never sleeps, so it’s easy to see the time and other important information, without raising or tapping the display. New location features, from a built-in compass to current elevation, help users better navigate their day, while international emergency calling1 allows customers to call emergency services directly from Apple Watch in over 150 countries, even without iPhone nearby.  is available in a wider range of materials, including aluminium, stainless steel, ceramic and an all-new titanium.",
            "brand": "Tile",
            "available": true,
            "colors": ["red", "purple", "green"]
        },
        {
            "id":24,
            "name": "Ronyes Unisex College Bag Bookbags for Women",
            "price": 23.99,
            "rating": 2,
            "img": "https://pixinvent.com/demo/vuexy-vuejs-admin-dashboard-template/demo-1/img/24.79a14740.png",
            "discription": "On Retina display that never sleeps, so it’s easy to see the time and other important information, without raising or tapping the display. New location features, from a built-in compass to current elevation, help users better navigate their day, while international emergency calling1 allows customers to call emergency services directly from Apple Watch in over 150 countries, even without iPhone nearby.  is available in a wider range of materials, including aluminium, stainless steel, ceramic and an all-new titanium.",
            "brand": "Ronyes",
            "available": true,
            "colors": ["red", "purple", "green"]
        },
        {
            "id":25,
            "name": "Willful Smart Watch for Men Women 2020,",
            "price": 29.99,
            "rating": 5,
            "img": "https://pixinvent.com/demo/vuexy-vuejs-admin-dashboard-template/demo-1/img/25.e1f92d21.png",
            "discription": "On Retina display that never sleeps, so it’s easy to see the time and other important information, without raising or tapping the display. New location features, from a built-in compass to current elevation, help users better navigate their day, while international emergency calling1 allows customers to call emergency services directly from Apple Watch in over 150 countries, even without iPhone nearby.  is available in a wider range of materials, including aluminium, stainless steel, ceramic and an all-new titanium.",
            "brand": "Willful",
            "available": true,
            "colors": ["red", "purple", "green"]
        },
        {
            "id":26,
            "name": "VicTsing Wireless Mouse,",
            "price": 10.99,
            "rating": 3,
            "img": "https://pixinvent.com/demo/vuexy-vuejs-admin-dashboard-template/demo-1/img/27.9b4c2313.png",
            "discription": "On Retina display that never sleeps, so it’s easy to see the time and other important information, without raising or tapping the display. New location features, from a built-in compass to current elevation, help users better navigate their day, while international emergency calling1 allows customers to call emergency services directly from Apple Watch in over 150 countries, even without iPhone nearby.  is available in a wider range of materials, including aluminium, stainless steel, ceramic and an all-new titanium.",
            "brand": "VicTsing",
            "available": true,
            "colors": ["red", "purple", "green"]
        },
        {
            "id":27,
            "name": "Bose Frames Tenor - Rectangular Polarized, Bluetooth Audio Sunglasses",
            "price": 249,
            "rating": 4,
            "img": "https://pixinvent.com/demo/vuexy-vuejs-admin-dashboard-template/demo-1/img/26.257af602.png",
            "discription": "On Retina display that never sleeps, so it’s easy to see the time and other important information, without raising or tapping the display. New location features, from a built-in compass to current elevation, help users better navigate their day, while international emergency calling1 allows customers to call emergency services directly from Apple Watch in over 150 countries, even without iPhone nearby.  is available in a wider range of materials, including aluminium, stainless steel, ceramic and an all-new titanium.",
            "brand": "Bose",
            "available": true,
            "colors": ["red", "purple", "green"]
        }],
            selected_data:[],
            arr:[],
            search:'',
            block:"none",
             open:"block",
             show:false,
             brand:"",
             current: 1,
              paginate: 5,
              paginate_total: 0
        }
    },
 
    mounted(){
       
    // fetch('http://localhost:3000/products')
    // .then((res)=> res.clone().json())
    // .then((data)=> { 
    //  this.products=data
    //  this.arr=data
    
    // }).catch(err => console.log(" error found"+err.message))
    
       this.arr=this.products  
    },
    
     methods:{
       fun(){
         console.log("ddddd")
       },
      opencart(){
            this.block="block"  
            this.open="none"
      },
       closeCart(){
            this.block="none"  
            this.open="block"
      },
       openside(){
       this.toggle=true;
       this.show=true
        },
         closeSide(){
           this.toggle=false;
           this.show=false
         },
      // opentoggle(){
      //   this.flag= !this.flag
      // },
     
      onChange(event){
        this.All = event.target.value;
            
      },
      displayAll(){
           this.arr=this.products
           return this.arr
      },
      displayless(){
          this.selected_data =this.products.filter((item)=>{ 
             return item.price <=10 
         })
         this.arr=this.selected_data
           console.log("dddddd" + this.arr)
          return this.arr 
      },
      displayMore(){
        this.selected_data =this.products.filter((item)=>{ 
             return (item.price <= 100 && item.price >= 10 )
         })
         this.arr=this.selected_data
          return this.arr 
      },
       displayMore2(){
        this.selected_data =this.products.filter((item)=>{ 
             return (item.price <= 500 && item.price >= 100 )
         })
         this.arr=this.selected_data
          return this.arr 
      },
      
      displayMore3(){
        this.selected_data =this.products.filter((item)=>{ 
             return ( item.price >= 500 )
         })
         this.arr=this.selected_data
          return this.arr 
      },
       searchFun(){
         this.selected_data =this.products.filter((item)=>{
           return item.name.toLowerCase().includes(this.search.toLowerCase())
         })
         this.arr=this.selected_data
         console.log("computed")
         return this.arr
       },
        selectFun(){

           if(this.role=="Lowtest")
           this.arr.sort((a, b) => a.price - b.price );

           else if(this.role == "Highest")
           this.arr.sort((a, b) => b.price - a.price );
             else  this.arr
         
         return this.arr
      },
      selectFromsidebar(){
          this.selected_data=filter((item)=>{
              if(Appliances =='Appliances'){
             return item.available=true
           }
           else{
             return  item.available =false
           }
          })
          this.arr=this.selected_data
          return this.arr
      },
      selectBrand(){
        this.selected_data =this.products.filter((item)=>{
          if(this.brand == "Insignia™"){
            return  item.brand.includes('Philips')
            }
            else if(this.brand == "Samsung"){
            return item.brand.includes('google')
            }
            else if(this.brand == "Apple"){
            return item.brand.includes('apple')
            }
            else if (this.brand == "Metra"){
            return item.brand.includes('Nike')
            }
            else return item.brand.includes('Adidas')
        })
         this.arr=this.selected_data
         return this.arr  
      }
    },
    computed:{ 
        
     },
}
</script>

<style  lang="scss">
.products{
 // background:black;
    margin: 1.3rem 2rem 0;
    margin-left:285px;
    position: relative;
   width: calc(100% - 4rem - 260px);
    min-height: calc(100% - 3.35rem);
    font-family: 'Segoe UI', Tahoma, sans-serif;
    transition: all .3s ease;
   
  .container1{
    width:100%; 
    display:flex;
    justify-content:space-between;
    .checkbox,.checkbox1{
        width:260px;
        height:70%;
        background-color: #fff;
        box-shadow: 0 0 15px 0 rgb(34 41 47 / 5%);
        border-radius:0.3rem;
        color:#625f6ecb;
        padding: 1.5rem;
        margin-right:5%;
        
        ul{
            margin:0;
            padding:0;
         li h2 {
          margin-bottom:1rem;
          margin-top:1rem;
           font-size: 1rem;
           font-family: inherit;
           font-weight: 500;
           line-height: 1.2;
           color: #5e5873e7;
          }
          
          li{
                 svg[fill="none"]{
                    color:#b9b9c3; 
                 }
               svg{
               color:#e29609; }
               span{
                 color:#7367f0;
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

/* When the radio button is checked, add a blue background */
.labal input:checked ~ .checkmark {
  background-color: #7367f0;
}
    }
  
}
 ///////////////////overlay///////////
 .sidenav-overlay{
  background-color: rgba(34,41,47,.5);
   position: fixed;
    top: 0;
    left: 0;
    right: 0;
    height: 100%;
    z-index: 997;
    // display: block;
    // visibility: hidden;
    // opacity: 0;
    -webkit-transition: all .5s ease;
    transition: all .5s ease;
    .checkbox1{
      position:absolute;
      left:0;
      height: 100%;
      overflow:none;
    }
    .overlay-side{
       height: 100%;
       position:absolute;
       right:0;
      width:70%;

    }
}
.show{
  display:block !important;
} 
}

/////////////////////////////////////////////////////////////////
.filter{
    //background-color:red;
   font-family: 'Segoe UI', Tahoma, sans-serif;
    position: relative;
    width:100%; 
    display:flex;
   justify-content:flex-end;
   color:#625f6e;
   font-size:1rem;
  
  .content{
   width: 100%;
   display:flex;
   justify-content: space-between;
   .filter-content {
    width: 260px;
    margin-left: 1rem;
      .par_toggle{
        display:none;
      }
    
  }///end
  form{
     display:flex;
  }
  select {
  text-align:left;
  padding:  10px 20px;
  border: 1px solid #7367f0 ;
  border-radius: 4px;
  background-color: #fff;
  outline: none;
  color:#7367f0;
  font-size: 14px;
 
} 
  .setting{
    // background-color:#7367f0;
    margin-right:0.9rem;
    width:75%;
    display:flex;
    justify-content:space-between;
    button{
      background-color:#7367f0;
      padding:0.8rem;
      border-radius: 10px;
      border: none;
      svg{
        color:#fff;
      }
    }
    ////////////////////////
    .switch-field {
	display: flex;
	margin-bottom: 36px;
	overflow: hidden;
    margin-left: 10px;
}

.switch-field input {
	position: absolute !important;
	//clip: rect(0, 0, 0, 0);
    height: 1px;
	width: 1px;
	border: 0;
	overflow: hidden;
}

.switch-field label {
	background-color: #fff;
	font-size: 14px;
	line-height: 1;
	text-align: center;
	padding: 9px 15px;
	margin-right: 0px;
	border: 1px solid #7367f0 ;
  border-radius: 0.357rem;
//	box-shadow: inset 0 1px 3px rgba(0, 0, 0, 0.3), 0 1px rgba(255, 255, 255, 0.1);
	transition: all 0.1s ease-in-out;
  svg{
    color:#7367f0 ;
  }
}

.switch-field label:hover {
	cursor: pointer;
}

.switch-field input:checked + label {
    background-color: rgba(115,103,240,.2);
	box-shadow: none;
}

.switch-field label:first-of-type {
	border-radius: 4px 0 0 4px;
    border-right: none;
}

.switch-field label:last-of-type {
	border-radius: 0 4px 4px 0;
}
  }
    }
    
}
////////////////////////////////////////////////////
 .cards{
     // background-color: cyan;
      font-family: 'Segoe UI', Tahoma, sans-serif;
     width:72%;
     display:flex;
    .shop-cards{
    width:100%;
    position: relative;
    display:flex;
    flex-wrap: wrap;
    flex-direction: row;
    justify-content:space-between;
    box-sizing: border-box;
    overflow: hidden;
    .search{
        width:100%;
        text-align: center;
        margin-bottom:1rem;
        input{
            
            width:100%;
            padding: 15px 20px;
            margin-bottom:10px;
             display: inline-block;
           border:none;
           box-shadow: 0 2px 8px 0 rgb(34 41 47 / 14%);
            border-radius: 0.3rem;
            box-sizing: border-box;
            outline: none;
            padding-left: 1.25rem;
            height: 48px;
            font-size: .95rem;
        }
    }
     } 
   .card:hover{
   transform: translateY(-15px);
  -webkit-transform: translateY(-15px);
  -moz-transform: translateY(-15px);
  -ms-transform: translateY(-15px);
  -o-transform: translateY(-15px);
  background:#fff;
       }
  .card {
      position: relative;
      display:flex;
      flex-direction: column;
      word-wrap: break-word;
   font-family: 'Segoe UI', Tahoma, sans-serif;
   transition: 0.3s;
   width:31%;
   border-radius: 0.428rem;
    margin-bottom: 1.5rem;
   background-color: #fff;
   background-clip: border-box;
   box-shadow: 0 4px 24px 0 rgb(34 41 47 / 10%);
    overflow: hidden;
     transition: all .3s ease-in-out;
     height:410px;
      
  .card-content {
    width:100%;
    height:100%;
    //display:flex;
     color: #5e5873;
      .price{
         width:100%;
           height:100%;
       box-sizing:border-box;
       width:100%;
       position:relative;
       display:flex;
       flex-direction: column;
      align-items:space-between;
       .price-content{
               .rating{
          word-wrap: break-word;
         display:flex;
         justify-content:space-between;
         ul{
           display: flex;
           li{
                svg{
                 color:#ff9f43;
                   }
             margin-right: 2px;
           }
         }
         .price1{
           font-weight: 600;
           margin-bottom: 0.5rem;
           font-size: 1rem;
          
         }
       }
           .discription{
           margin-top: 0.2rem;
           overflow: hidden;
           white-space: nowrap;
           text-overflow: ellipsis;
           font-size: .875rem;
             }
        .item-name{
         a{
          font-weight: 500;
         line-height: 1.2;
          margin-top: 0.75rem;
          text-decoration: none;
         font-size: 1rem;
          color: #5e5873;
          overflow: hidden;
           white-space: nowrap;
           font-weight: 600;
           display: -webkit-box;
          -webkit-line-clamp: 1;
         -webkit-box-orient: vertical;
          overflow: hidden;
           text-overflow: ellipsis
         }
       }
       }
     
       .card-button{
         .items-button{
           margin-bottom:0px;
           .Wishlist , .cart{
           text-align: center;
           display:block;
           padding: 0.660rem 1.5rem;
           color: #2a2e30;
          background-color: #f6f6f6;
          border-color: #f6f6f6;
          width:100%;
          }
         .Wishlist:hover {
            background-color: #e3e3e3;
             border-color: #ddd;
          }
          .cart{
          color:#fff;
           background:#7367f0;
      }
         }
            
       }
    }
    a{
      text-decoration: none;
    }
  }
      
}
   }
/////////////////////////////////

.cart{
    font-family: 'Segoe UI', Tahoma, sans-serif;
    display:flex;
    justify-content:center;
    width:100%;
     color:#625f6e ;
     margin-bottom: 2rem;
     border: none;
    background:#fff;
    box-shadow: 0 4px 24px 0 rgb(34 41 47 / 10%);
     border-radius: 0.428rem;
      transition: all .3s ease-in-out;
      margin-bottom:1.5rem;
   .cart-content{
     display:flex;
       height:250px;
      overflow:hidden;

   }
   .block-img{
     display:flex;
     align-items:center;
     text-align: center;
      width:25%;
     // background:red;
      img{
        width:100%;
      }
    }
    .block2{
      padding:10px 10px;
      width:25%;
       text-align: center;
       border-left:1px solid #6363635b;
      a{
      text-decoration: none;
  }
  
   
   .Wishlist , .cart{
          text-align: center;
           display:block;
          padding:10px 0px;
          background:#d6d5db62;
          border-radius:5px;
          width:100%;
         // height:;
          color: rgb(54, 53, 53);
          margin-top:10px;
      }
      .cart{
         background: #7367f0;
         color: #fff;
      }
    }
    .discription{
      display: -webkit-box;   
   -webkit-line-clamp: 5;   
   -webkit-box-orient: vertical;     
   overflow: hidden; 
   font-weight: 400;
    line-height: 1.45;
    color: #6e6b7b;
    }
   .block1{
     
     box-sizing:border-box;
       width:50%;
       padding:10px 5px;
     font-size: 14px;
      
     svg{
       color:#e29609;
     }
     a{
        color:#625f6eee ;
        text-decoration: none;
     }
   }
  }
  .cart:hover{
   transform: translateY(-15px);
  -webkit-transform: translateY(-15px);
  -moz-transform: translateY(-15px);
  -ms-transform: translateY(-15px);
  -o-transform: translateY(-15px);
  background:#fff;
       }
  .cartHorizental{
    display:none;
  }
  ::placeholder { 
 color:#5e5873af;
      }
      @media screen and (max-width:950px) {
  .products{
      width:96%;
     margin-left:25px;
      .checkbox{
    display:none !important;
       }
       .cards{
         width:98%;
       }
  }
   .shop-cards{
     flex-direction: column;
   }
  //  .card {
  //    width:45% !important;
  //    //margin-right:5px;
  //  }
   .filter{
   justify-content:center;
  // background:red;
    .pargr{
      display:none ;
    }
    .par_toggle{
      display:block !important;
      color:rgb(102, 93, 93);
    }}
    .found{
     display:none;
   }
}
 @media screen and (max-width:590px) {
   .shop-cards{
     flex-direction: column;
   }
   .card {
     width:95% !important;
     margin-right:5px;
   }
  
 
 }
</style>