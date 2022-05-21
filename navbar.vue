<template>
  <nav class="navbar" :class="danger">
      <div class="navbar-container">
          <div style="display:none" class="toggle">
             <ul>
                 <li> <a href="#" target="_self" @click="openside"><svg xmlns="http://www.w3.org/2000/svg" width="21px" height="21px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-menu"><line x1="3" y1="12" x2="21" y2="12"></line><line x1="3" y1="6" x2="21" y2="6"></line><line x1="3" y1="18" x2="21" y2="18"></line></svg></a></li>
             </ul>
          </div>
        <div class="navbar-left">
           <ul>
             <li><a  href="#"><svg data-v-1134b199="" xmlns="http://www.w3.org/2000/svg" width="21px" height="21px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-calendar"><rect data-v-1134b199="" x="3" y="4" width="18" height="18" rx="2" ry="2"></rect><line data-v-1134b199="" x1="16" y1="2" x2="16" y2="6"></line><line data-v-1134b199="" x1="8" y1="2" x2="8" y2="6"></line><line data-v-1134b199="" x1="3" y1="10" x2="21" y2="10"></line></svg></a></li>
             <li><a  href="#"><svg data-v-1134b199="" xmlns="http://www.w3.org/2000/svg" width="21px" height="21px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-message-square"><path data-v-1134b199="" d="M21 15a2 2 0 0 1-2 2H7l-4 4V5a2 2 0 0 1 2-2h14a2 2 0 0 1 2 2z"></path></svg></a></li>
             <li><a  href="#"><svg data-v-1134b199="" xmlns="http://www.w3.org/2000/svg" width="21px" height="21px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-mail"><path data-v-1134b199="" d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"></path><polyline data-v-1134b199="" points="22,6 12,13 2,6"></polyline></svg></a></li>
             <li><a  href="#"><svg data-v-1134b199="" xmlns="http://www.w3.org/2000/svg" width="21px" height="21px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-check-square"><polyline data-v-1134b199="" points="9 11 12 14 22 4"></polyline><path data-v-1134b199="" d="M21 12v7a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V5a2 2 0 0 1 2-2h11"></path></svg></a></li>
             <li><a  href="#" class="star"><svg data-v-1134b199="" xmlns="http://www.w3.org/2000/svg" width="21px" height="21px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="text-warning feather feather-star"><polygon data-v-1134b199="" points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon></svg></a></li>
           </ul>
          </div>
          <div class="navbar-right">
         <ul>
          <li class="dropdown">
         <a href="#"><img class="image" alt="logo" src="../assets/download.png">
         <span class="lang">English</span></a>
         <ul class="dropdown-content">
           <li><a href="#"><img class="image" alt="logo" src="../assets/download.png">
         <span class="lang">English</span></a></li>
          <li><a href="#"><img class="image" alt="logo" src="../assets/download4.png">
         <span class="lang">French</span></a></li>
          <li><a href="#"><img class="image" alt="logo" src="../assets/download3.png">
         <span class="lang">German</span></a></li>
          <li><a href="#"><img class="image" alt="logo" src="../assets/download2.png">
         <span class="lang">Portugu</span></a></li>  
            </ul>   </li>
          <li v-if="active"><a @click="chandeMode" href="#"><svg xmlns="http://www.w3.org/2000/svg" width="21px" height="21px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-moon"><path d="M21 12.79A9 9 0 1 1 11.21 3 7 7 0 0 0 21 12.79z"></path></svg></a></li>
          <li v-if="!active"><a @click="returnMode" href="#"><svg xmlns="http://www.w3.org/2000/svg" width="21px" height="21px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-sun"><circle cx="12" cy="12" r="5"></circle><line x1="12" y1="1" x2="12" y2="3"></line><line x1="12" y1="21" x2="12" y2="23"></line><line x1="4.22" y1="4.22" x2="5.64" y2="5.64"></line><line x1="18.36" y1="18.36" x2="19.78" y2="19.78"></line><line x1="1" y1="12" x2="3" y2="12"></line><line x1="21" y1="12" x2="23" y2="12"></line><line x1="4.22" y1="19.78" x2="5.64" y2="18.36"></line><line x1="18.36" y1="5.64" x2="19.78" y2="4.22"></line></svg></a></li>
          <li><a href="#"><svg data-v-0e8a7f4f="" xmlns="http://www.w3.org/2000/svg" width="21px" height="21px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-search"><circle data-v-0e8a7f4f="" cx="11" cy="11" r="8"></circle><line data-v-0e8a7f4f="" x1="21" y1="21" x2="16.65" y2="16.65"></line></svg></a></li>
          <li><a href="#"><svg xmlns="http://www.w3.org/2000/svg" width="21px" height="21px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="text-body feather feather-bell"><path d="M18 8A6 6 0 0 0 6 8c0 7-3 9-3 9h18s-3-2-3-9"></path><path d="M13.73 21a2 2 0 0 1-3.46 0"></path></svg></a></li>
          <li class="notfication hide"><a href="#"><svg data-v-a58fee00="" xmlns="http://www.w3.org/2000/svg" width="21px" height="21px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="text-body feather feather-shopping-cart"><circle data-v-a58fee00="" cx="9" cy="21" r="1"></circle><circle data-v-a58fee00="" cx="20" cy="21" r="1"></circle><path data-v-a58fee00="" d="M1 1h4l2.68 13.39a2 2 0 0 0 2 1.61h9.72a2 2 0 0 0 2-1.61L23 6H6"></path></svg>
          <span class="notify " >5</span></a></li>
          <li class="notfication hide"><a href="#"><svg xmlns="http://www.w3.org/2000/svg" width="21px" height="21px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="text-body feather feather-bell"><path d="M18 8A6 6 0 0 0 6 8c0 7-3 9-3 9h18s-3-2-3-9"></path><path d="M13.73 21a2 2 0 0 1-3.46 0"></path></svg>
              <span class="notify" style="background:#ea5455">6</span> </a></li>
            <li style=" ">
                 <div class="nav2">
                 <span style="margin-right:0.3rem" class="content"><p style="font-weight:bold;">Jone Doe </p>
                 <span class="admin">admin</span>
                </span>
                <span > <a href="#"><img  alt="logo" src="../assets/13-small.d796bffd.png" ><span class="active" ></span>
                </a> </span>
                </div>
               
            </li>
   </ul>
          </div>
      </div>
  </nav>

  <!-- side nav    :style="{display:showSidbar}" -->
  <div class="sidenav" :class="{show:block}" v-if="showSidbar">
    <div class="sidnav-header">
      <ul class="brand">
        <li class="logo">
          <a href="#">
             <img alt="Vue logo" src="../assets/logo3.svg">
             <h2> Vuexy </h2>
          </a>
        </li>
        <li class="nav1">
          <a>
           <svg @click="closeSide" xmlns="http://www.w3.org/2000/svg" width="20px" height="20px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather" style="display:none" :class="{show:block}"><line x1="18" y1="6" x2="6" y2="18"></line><line x1="6" y1="6" x2="18" y2="18"></line></svg>
           <svg  xmlns="http://www.w3.org/2000/svg" width="20px" height="20px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" style="display:block" class="closetoggle"><circle cx="12" cy="12" r="10"></circle><circle cx="12" cy="12" r="3"></circle></svg>
          </a>
        </li>
      </ul>
    </div>
    <div class="links">
      <ul>
        <li class="dashboard">
          <a href="#" class="dashboard_logo" @click="displayLinks"><svg xmlns="http://www.w3.org/2000/svg" width="20px" height="20px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class=""><path d="M3 9l9-7 9 7v11a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2z"></path><polyline points="9 22 9 12 15 12 15 22"></polyline></svg>
          <span>Dashboards</span>
          <span class="span1"> 2  </span>
          <span style="display:inline-block; position:relative"><svg class="svg-icon" viewBox="0 0 20 20">
							<path fill="gray" d="M11.611,10.049l-4.76-4.873c-0.303-0.31-0.297-0.804,0.012-1.105c0.309-0.304,0.803-0.293,1.105,0.012l5.306,5.433c0.304,0.31,0.296,0.805-0.012,1.105L7.83,15.928c-0.152,0.148-0.35,0.223-0.547,0.223c-0.203,0-0.406-0.08-0.559-0.236c-0.303-0.309-0.295-0.803,0.012-1.104L11.611,10.049z"></path>
						</svg></span>
            <!-- <span :class="{show:block}" style="display:none"><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-chevron-down" viewBox="0 0 16 16">
              <path fill-rule="evenodd" d="M1.646 4.646a.5.5 0 0 1 .708 0L8 10.293l5.646-5.647a.5.5 0 0 1 .708.708l-6 6a.5.5 0 0 1-.708 0l-6-6a.5.5 0 0 1 0-.708z"/>
           </svg></span> -->
          </a>
        <ul class="dashboard-links" v-if="flag"> 
        <li>
         <a href="#"><svg xmlns="http://www.w3.org/2000/svg" width="14px" height="14px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-circle"><circle cx="12" cy="12" r="10"></circle></svg> 
         <span>ecommerce</span></a>
         </li>
         <li>
         <a href="#"><svg xmlns="http://www.w3.org/2000/svg" width="14px" height="14px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-circle"><circle cx="12" cy="12" r="10"></circle></svg> 
         <span>Analytics</span></a>
         </li>
        </ul> 
        </li>

      </ul>
        <ul class="app_link">
       <li> <span class="title">APP  &amp; PAGES</span> </li>
       <li class=""><a href="#"><svg xmlns="http://www.w3.org/2000/svg" width="14px" height="14px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-mail"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"></path><polyline points="22,6 12,13 2,6"></polyline></svg>Email</a></li>
       <li class=""><a href="#"><svg xmlns="http://www.w3.org/2000/svg" width="14px" height="14px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-circle"><circle cx="12" cy="12" r="10"></circle></svg>Details</a></li>
       <li class=""><a href="#" class="d-flex align-items-center"><svg xmlns="http://www.w3.org/2000/svg" width="14px" height="14px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-check-square"><polyline points="9 11 12 14 22 4"></polyline><path d="M21 12v7a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V5a2 2 0 0 1 2-2h11"></path></svg>Todo</a></li>
       <li class=""><a href="/demo/vuexy-vuejs-admin-dashboard-template/demo-1/apps/calendar" class="d-flex align-items-center"><svg xmlns="http://www.w3.org/2000/svg" width="14px" height="14px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-calendar"><rect x="3" y="4" width="18" height="18" rx="2" ry="2"></rect><line x1="16" y1="2" x2="16" y2="6"></line><line x1="8" y1="2" x2="8" y2="6"></line><line x1="3" y1="10" x2="21" y2="10"></line></svg>Calendar</a></li>
       <li class="" @click="click2"><a href="/demo/vuexy-vuejs-admin-dashboard-template/demo-1/apps/calendar" class="d-flex align-items-center"><svg xmlns="http://www.w3.org/2000/svg" width="14px" height="14px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-file-text"><path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"></path><polyline points="14 2 14 8 20 8"></polyline><line x1="16" y1="13" x2="8" y2="13"></line><line x1="16" y1="17" x2="8" y2="17"></line><polyline points="10 9 9 9 8 9"></polyline></svg>Invoice <span style="display:inline-block; position:relative"><svg class="svg-icon" viewBox="0 0 20 20">
						<path fill="gray" d="M11.611,10.049l-4.76-4.873c-0.303-0.31-0.297-0.804,0.012-1.105c0.309-0.304,0.803-0.293,1.105,0.012l5.306,5.433c0.304,0.31,0.296,0.805-0.012,1.105L7.83,15.928c-0.152,0.148-0.35,0.223-0.547,0.223c-0.203,0-0.406-0.08-0.559-0.236c-0.303-0.309-0.295-0.803,0.012-1.104L11.611,10.049z"></path>
						</svg></span></a>
        
        <ul class="sub_links" v-if="flag2"> 
        <li>
         <a href="#"><svg xmlns="http://www.w3.org/2000/svg" width="14px" height="14px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-circle"><circle cx="12" cy="12" r="10"></circle></svg> 
         <span>List</span></a>
         </li>
         <li>
         <a href="#"><svg xmlns="http://www.w3.org/2000/svg" width="14px" height="14px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-circle"><circle cx="12" cy="12" r="10"></circle></svg> 
         <span>Preview</span></a>
         </li>
          <li>
         <a href="#"><svg xmlns="http://www.w3.org/2000/svg" width="14px" height="14px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-circle"><circle cx="12" cy="12" r="10"></circle></svg> 
         <span>Edit</span></a>
         </li>
          <li>
         <a href="#"><svg xmlns="http://www.w3.org/2000/svg" width="14px" height="14px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-circle"><circle cx="12" cy="12" r="10"></circle></svg> 
         <span>Add</span></a>
         </li>
        </ul> 
       </li>
       <li class="" @click.prevent="click1"><a href="/demo/vuexy-vuejs-admin-dashboard-template/demo-1/apps/calendar" class="d-flex align-items-center"><svg xmlns="http://www.w3.org/2000/svg" width="14px" height="14px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-shopping-cart"><circle cx="9" cy="21" r="1"></circle><circle cx="20" cy="21" r="1"></circle><path d="M1 1h4l2.68 13.39a2 2 0 0 0 2 1.61h9.72a2 2 0 0 0 2-1.61L23 6H6"></path></svg>ecommerce
        </a>
        <ul class="sub_links" v-if="flag1"> 
        <li>
         <a href="#"><svg xmlns="http://www.w3.org/2000/svg" width="14px" height="14px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-circle"><circle cx="12" cy="12" r="10"></circle></svg> 
         <span>List</span></a>
         </li>
         <li>
         <a href="#"><svg xmlns="http://www.w3.org/2000/svg" width="14px" height="14px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-circle"><circle cx="12" cy="12" r="10"></circle></svg> 
         <span>Preview</span></a>
         </li>
          <li>
         <a href="#"><svg xmlns="http://www.w3.org/2000/svg" width="14px" height="14px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-circle"><circle cx="12" cy="12" r="10"></circle></svg> 
         <span>Edit</span></a>
         </li>
          <li>
         <a href="#"><svg xmlns="http://www.w3.org/2000/svg" width="14px" height="14px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-circle"><circle cx="12" cy="12" r="10"></circle></svg> 
         <span>Add</span></a>
         </li>
        </ul> 
       </li>
      <li class=""><a href="/demo/vuexy-vuejs-admin-dashboard-template/demo-1/apps/calendar" class="d-flex align-items-center"><svg xmlns="http://www.w3.org/2000/svg" width="14px" height="14px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-user"><path d="M20 21v-2a4 4 0 0 0-4-4H8a4 4 0 0 0-4 4v2"></path><circle cx="12" cy="7" r="4"></circle></svg>User</a></li>
      <li class=""><a href="/demo/vuexy-vuejs-admin-dashboard-template/demo-1/apps/calendar" class="d-flex align-items-center"><svg xmlns="http://www.w3.org/2000/svg" width="14px" height="14px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-user"><path d="M20 21v-2a4 4 0 0 0-4-4H8a4 4 0 0 0-4 4v2"></path><circle cx="12" cy="7" r="4"></circle></svg>Pages</a></li>
      <li><span class="title">User Interface</span></li>
      <li class=""><a href="/demo/vuexy-vuejs-admin-dashboard-template/demo-1/apps/calendar" class="d-flex align-items-center"><svg xmlns="http://www.w3.org/2000/svg" width="14px" height="14px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-type"><polyline points="4 7 4 4 20 4 20 7"></polyline><line x1="9" y1="20" x2="15" y2="20"></line><line x1="12" y1="4" x2="12" y2="20"></line></svg>Typography</a></li>
      <li class=""><a href="/demo/vuexy-vuejs-admin-dashboard-template/demo-1/apps/calendar" class="d-flex align-items-center"><svg xmlns="http://www.w3.org/2000/svg" width="14px" height="14px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-droplet"><path d="M12 2.69l5.66 5.66a8 8 0 1 1-11.31 0z"></path></svg>Colors</a></li>
      <li class=""><a href="/demo/vuexy-vuejs-admin-dashboard-template/demo-1/apps/calendar" class="d-flex align-items-center"><svg xmlns="http://www.w3.org/2000/svg" width="14px" height="14px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-eye"><path d="M1 12s4-8 11-8 11 8 11 8-4 8-11 8-11-8-11-8z"></path><circle cx="12" cy="12" r="3"></circle></svg>Feather</a></li>
      <li class=""><a href="/demo/vuexy-vuejs-admin-dashboard-template/demo-1/apps/calendar" class="d-flex align-items-center"><svg xmlns="http://www.w3.org/2000/svg" width="14px" height="14px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-credit-card"><rect x="1" y="4" width="22" height="16" rx="2" ry="2"></rect><line x1="1" y1="10" x2="23" y2="10"></line></svg>Cards</a></li>
      <li class=""><a href="/demo/vuexy-vuejs-admin-dashboard-template/demo-1/apps/calendar" class="d-flex align-items-center"><svg xmlns="http://www.w3.org/2000/svg" width="14px" height="14px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-archive"><polyline points="21 8 21 21 3 21 3 8"></polyline><rect x="1" y="3" width="22" height="5"></rect><line x1="10" y1="12" x2="14" y2="12"></line></svg>Components</a></li>
      <li class=""><a href="/demo/vuexy-vuejs-admin-dashboard-template/demo-1/apps/calendar" class="d-flex align-items-center"><svg xmlns="http://www.w3.org/2000/svg" width="14px" height="14px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-plus-circle"><circle cx="12" cy="12" r="10"></circle><line x1="12" y1="8" x2="12" y2="16"></line><line x1="8" y1="12" x2="16" y2="12"></line></svg>Extensions</a></li>
      <li class=""><a href="/demo/vuexy-vuejs-admin-dashboard-template/demo-1/apps/calendar" class="d-flex align-items-center"><svg xmlns="http://www.w3.org/2000/svg" width="14px" height="14px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-layout"><rect x="3" y="3" width="18" height="18" rx="2" ry="2"></rect><line x1="3" y1="9" x2="21" y2="9"></line><line x1="9" y1="21" x2="9" y2="9"></line></svg>Page Layouts</a></li>
       <li><span class="title">Forms &amp; Tables</span></li>
      <li class=""><a href="/demo/vuexy-vuejs-admin-dashboard-template/demo-1/apps/calendar" class="d-flex align-items-center"><svg xmlns="http://www.w3.org/2000/svg" width="14px" height="14px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-copy"><rect x="9" y="9" width="13" height="13" rx="2" ry="2"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path></svg>Form elements</a></li>
      <li class=""><a href="/demo/vuexy-vuejs-admin-dashboard-template/demo-1/apps/calendar" class="d-flex align-items-center"><svg xmlns="http://www.w3.org/2000/svg" width="14px" height="14px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-copy"><rect x="9" y="9" width="13" height="13" rx="2" ry="2"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path></svg>Form Layout</a></li>
      <li class=""><a href="/demo/vuexy-vuejs-admin-dashboard-template/demo-1/apps/calendar" class="d-flex align-items-center"><svg xmlns="http://www.w3.org/2000/svg" width="14px" height="14px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-package"><line x1="16.5" y1="9.4" x2="7.5" y2="4.21"></line><path d="M21 16V8a2 2 0 0 0-1-1.73l-7-4a2 2 0 0 0-2 0l-7 4A2 2 0 0 0 3 8v8a2 2 0 0 0 1 1.73l7 4a2 2 0 0 0 2 0l7-4A2 2 0 0 0 21 16z"></path><polyline points="3.27 6.96 12 12.01 20.73 6.96"></polyline><line x1="12" y1="22.08" x2="12" y2="12"></line></svg>Form Wizard</a></li>
      <li class=""><a href="/demo/vuexy-vuejs-admin-dashboard-template/demo-1/apps/calendar" class="d-flex align-items-center"><svg xmlns="http://www.w3.org/2000/svg" width="14px" height="14px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-package"><line x1="16.5" y1="9.4" x2="7.5" y2="4.21"></line><path d="M21 16V8a2 2 0 0 0-1-1.73l-7-4a2 2 0 0 0-2 0l-7 4A2 2 0 0 0 3 8v8a2 2 0 0 0 1 1.73l7 4a2 2 0 0 0 2 0l7-4A2 2 0 0 0 21 16z"></path><polyline points="3.27 6.96 12 12.01 20.73 6.96"></polyline><line x1="12" y1="22.08" x2="12" y2="12"></line></svg>Form Validation</a></li>
      <li class=""><a href="/demo/vuexy-vuejs-admin-dashboard-template/demo-1/apps/calendar" class="d-flex align-items-center"><svg xmlns="http://www.w3.org/2000/svg" width="14px" height="14px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-copy"><rect x="9" y="9" width="13" height="13" rx="2" ry="2"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path></svg>Form Repeater</a></li>
      <li class=""><a href="/demo/vuexy-vuejs-admin-dashboard-template/demo-1/apps/calendar" class="d-flex align-items-center"><svg xmlns="http://www.w3.org/2000/svg" width="14px" height="14px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-server"><rect x="2" y="2" width="20" height="8" rx="2" ry="2"></rect><rect x="2" y="14" width="20" height="8" rx="2" ry="2"></rect><line x1="6" y1="6" x2="6.01" y2="6"></line><line x1="6" y1="18" x2="6.01" y2="18"></line></svg>BS Table</a></li>
      <li class=""><a href="/demo/vuexy-vuejs-admin-dashboard-template/demo-1/apps/calendar" class="d-flex align-items-center"><svg xmlns="http://www.w3.org/2000/svg" width="14px" height="14px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-grid"><rect x="3" y="3" width="7" height="7"></rect><rect x="14" y="3" width="7" height="7"></rect><rect x="14" y="14" width="7" height="7"></rect><rect x="3" y="14" width="7" height="7"></rect></svg>Cood Table</a></li>
      <li><span class="title">Charts &amp; Maps</span></li>
      <li class=""><a href="/demo/vuexy-vuejs-admin-dashboard-template/demo-1/apps/calendar" class="d-flex align-items-center"><svg xmlns="http://www.w3.org/2000/svg" width="14px" height="14px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-pie-chart"><path d="M21.21 15.89A10 10 0 1 1 8 2.83"></path><path d="M22 12A10 10 0 0 0 12 2v10z"></path></svg>Charts</a></li>
      <li class=""><a href="/demo/vuexy-vuejs-admin-dashboard-template/demo-1/apps/calendar" class="d-flex align-items-center"><svg xmlns="http://www.w3.org/2000/svg" width="14px" height="14px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-map"><polygon points="1 6 1 22 8 18 16 22 23 18 23 2 16 6 8 2 1 6"></polygon><line x1="8" y1="2" x2="8" y2="18"></line><line x1="16" y1="6" x2="16" y2="22"></line></svg> Leaflet</a></li>
      <li><span class="title">OTHERS</span></li>
      <li class=""><a href="/demo/vuexy-vuejs-admin-dashboard-template/demo-1/apps/calendar" class="d-flex align-items-center"><svg xmlns="http://www.w3.org/2000/svg" width="14px" height="14px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-shield"><path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"></path></svg>Access Control</a></li>
      <li class=""><a href="/demo/vuexy-vuejs-admin-dashboard-template/demo-1/apps/calendar" class="d-flex align-items-center"><svg xmlns="http://www.w3.org/2000/svg" width="14px" height="14px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-menu"><line x1="3" y1="12" x2="21" y2="12"></line><line x1="3" y1="6" x2="21" y2="6"></line><line x1="3" y1="18" x2="21" y2="18"></line></svg>Menu Levels</a></li>
      <li class=""><a href="/demo/vuexy-vuejs-admin-dashboard-template/demo-1/apps/calendar" class="d-flex align-items-center"><svg xmlns="http://www.w3.org/2000/svg" width="14px" height="14px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-eye-off"><path d="M17.94 17.94A10.07 10.07 0 0 1 12 20c-7 0-11-8-11-8a18.45 18.45 0 0 1 5.06-5.94M9.9 4.24A9.12 9.12 0 0 1 12 4c7 0 11 8 11 8a18.5 18.5 0 0 1-2.16 3.19m-6.72-1.07a3 3 0 1 1-4.24-4.24"></path><line x1="1" y1="1" x2="23" y2="23"></line></svg>Disabled Menu</a></li>
      <li class=""><a href="/demo/vuexy-vuejs-admin-dashboard-template/demo-1/apps/calendar" class="d-flex align-items-center"> <svg xmlns="http://www.w3.org/2000/svg" width="14px" height="14px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-life-buoy"><circle cx="12" cy="12" r="10"></circle><circle cx="12" cy="12" r="4"></circle><line x1="4.93" y1="4.93" x2="9.17" y2="9.17"></line><line x1="14.83" y1="14.83" x2="19.07" y2="19.07"></line><line x1="14.83" y1="9.17" x2="19.07" y2="4.93"></line><line x1="14.83" y1="9.17" x2="18.36" y2="5.64"></line><line x1="4.93" y1="19.07" x2="9.17" y2="14.83"></line></svg>Raise Subbort</a></li>
      <li class=""><a href="/demo/vuexy-vuejs-admin-dashboard-template/demo-1/apps/calendar" class="d-flex align-items-center"><svg xmlns="http://www.w3.org/2000/svg" width="14px" height="14px" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-file-text"><path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"></path><polyline points="14 2 14 8 20 8"></polyline><line x1="16" y1="13" x2="8" y2="13"></line><line x1="16" y1="17" x2="8" y2="17"></line><polyline points="10 9 9 9 8 9"></polyline></svg> Documentation</a></li>
        </ul>
    </div>
  </div>
  <div class="sidenav-overlay" v-if="toggle"></div>
</template>

<script>
export default {
  name: 'HomeView',
  props:['danger','showSidbar'],
  data(){
    return{
      active:true,
      toggle:false,
        flag:false,
        block:false,
        openVar:true,
        closevar:false,
        flag1:false,
        flag2:false    }
  },
  components: {
   
  },
  methods:{
   displayLinks(){
       this.flag=!this.flag
       this.block="block"
   },
   click1(){
      this.flag1=!this.flag1
   },
   click2(){
      this.flag2=!this.flag2
   },
   chandeMode(){
      this.$emit("chandeMode",false);
      this.active=false;
   },
    returnMode(){
      this.$emit("chandeMode",true);
      this.active=true;
   },
   openside(){
       this.toggle=true;
       this.block=true
     },
         closeSide(){
           this.toggle=false;
           this.block=false
         }
  }
}
</script>

<style lang="scss">
.mode{
  display:none;
}
ul{
  list-style: none;
  margin:0;
  padding:0;
}
nav{
    top:0;
    padding:0;
    box-shadow: 0 4px 24px 0 rgb(34 41 47 / 10%);
    background:#fff;
    display: flex;
    position: fixed;
    width: calc(100% - 4rem - 260px);
    z-index: 12;
    height:4.1rem;
   font-family: 'Segoe UI', Tahoma, sans-serif;
    transition: all .3s ease;
     right:0.3rem;
    align-items: center;
    margin: 1.3rem 2rem 0;
    border-radius: 0.428rem;
    .navbar-container{
    min-height:62.38px;
    display: flex;
    padding: 0.8rem 1rem;
    width: 100%;
    align-items: center;
    //justify-content: space-between;
    
        ul{
         display: flex; 
         list-style: none;
         align-items: center;
         margin:0;
         padding:0;
         }
         .navbar-right{
            //background:chartreuse;
            width:481.26px;
            height:40px;
             display: flex;
             align-items: center;
             margin-left: auto;
             margin-right: 1rem;
             line-height:1.5rem;
             text-align: center;

             ul{
                 width:100%;
                margin: 0;
                padding: 0;
                display:flex;
                justify-content: space-between;
                align-items: center;
               // background:blue;
               .notfication{
                position: relative;
                    .notify{
                      font-weight: 600;
                       position: absolute;
                       top: -13px;
                       left:9px;
                       text-align: center;
                       min-width: 1.429rem;
                       min-height: 1.429rem;
                       display: flex;
                       justify-content: center;
                       font-size: .786rem;
                       line-height: 1.4rem;
                       color:#fff;
                       background:#7367f0;
                       border-radius:10px;
                    }
          }
      
             }
              li{
             a {
             display:inline-block;
             color: #565360;
             text-align: center;
             text-decoration: none;
              .image{
                width:22px;
                height:14px;
            }
              .lang{
                  font-family: 'Segoe UI', Tahoma, sans-serif;
               display:inline-block;
              color: #6e6b7bd8;
              font-size:1rem;
              margin-left: 7px;
              line-height: 1.5;
              }
             
           }
           ///////////////////////////////////////
            .nav2{
         display:flex;
         height:40px;
          
          line-height:0.3rem;
          color: #565365c4;
          position: relative;
          .content{
           font-family: 'Segoe UI', Tahoma, sans-serif;
              font-size:0.9rem;
               display:block;
               margin-top: -0.5rem;
             
          }
             .admin{
                margin-left: 1.4rem;
                display:block;
                 font-size:0.8rem;
                //background:red;
             }
              .active{
                       position: absolute;
                       min-width: 0.6rem;
                       min-height: 0.6rem;
                       display: block;
                       background:#72f067;
                       border-radius:10px;
                       right: 0.1rem;
                        top:1.9rem;
                        border:1px solid #fff;

                    } 
             img{
                 height:40px;
                 width:40px;
                 border-radius: 50%;
                 margin-left: 0.5rem;
                  position: relative;
                   display: inline-block;
             }
        }
        }
         }  
         .navbar-left{
             display: flex;
             width:630px;
             margin-right: auto;
             align-items: center;
            // background:red;
             
            ul{
                margin: 0px 15px;
                padding: 0;
                width:175px; 
                display:flex;
                justify-content: space-between;
                //background:black;
                li{
                   .star{color: #ff9f43; }
           a {
           display: block;
           color: #565360;
           text-align: center;
           text-decoration: none;
       
           }
           a:hover {
               color: #ff9f43;
              } 
       }    
            }
         }
         .toggle{
         width:25%;
         display:none;
         a {
             color: #565360;
            }
        }
   }
}

               
.dropdown {
  position: relative;
  display: inline-block;
}

   
.dropdown-content {
  display: none !important;
  position: absolute;
  background-color:#fff;
  min-width: 150px;
  min-height: 172px;
  box-shadow: 0 5px 25px rgb(34 41 47 / 10%);
  z-index: 1;
  border: 1px solid rgba(34,41,47,.05);
  padding: 9px 17px;
  //text-align: left;
  top: 55px!important;
  right:-2px;
 border-radius: 0.358rem;
  li{
      margin:15px 15px 0 0;
  }
}
.dropdown:hover .dropdown-content {display: block !important;}
/////////////////////////////sidnav/////////
.sidenav{
    position: fixed;
    width:260px;
    box-shadow: 0 0 15px 0 rgb(34 41 47 / 5%);
    background: #fff;
    color: #6e6b7b;
    display: table-cell;
    height: 100%;
    box-sizing: border-box;
    z-index: 1031;
    top:0;
    left:0;
    // overflow-x: hidden;
     scrollbar-color: #d4aa70 #e4e4e4;
     scrollbar-width: thin;
      overflow:hidden;;
    .sidnav-header{
   padding: 0.35rem 1rem 0.3rem 1.64rem;
   width: 260px;
    height: 4.45rem;
    position: relative;
   -webkit-transition: all .3s ease;
     transition: all .3s ease;
     display:flex;
     align-items: center;
     justify-content:center;
     .brand{
  //background:red;
  width: 260px;
  height:4rem;
  display:flex;
  list-style: none;
  padding:0;
  align-items: center;
  justify-content:center;

  .logo{
   margin-right: auto;
  a{
    text-decoration: none;
    img{
      max-width: 36px;
      height:24.47px;
      border-style: none;
      text-align: center;
    }
    
    h2{
     font-family: 'Segoe UI', Tahoma, sans-serif;
      display:inline;
      padding-left:0.7rem;
      color: #7367f0;
      font-weight: 600;
      letter-spacing: .01rem;
      font-size: 1.45rem;
      line-height: 1.2;
    }
  }
  
}
.nav1{
    a{
       color: #7367f0 !important;
    }
  }
}

}
}
.sidenav::-webkit-scrollbar {
  width: 10px;
}
.sidenav:hover {
   overflow-y: scroll;
}

.sidenav::-webkit-scrollbar-track {
  background-color: #e4e4e4;
  border-radius: 100px;
}

.sidenav::-webkit-scrollbar-thumb {
  border-radius: 100px;
  background:#87858f;
}
.links{
ul{
 // background:red;
 width:100%;
    font-size: 1.1rem;
    font-family: 'Segoe UI', Tahoma, sans-serif;
    font-weight: 400;
   // overflow-y: hidden;
    transition: transform .25s ease-in-out;
    padding:5px 10px;
    .dashboard:hover{
        transform: translateX(5px)!important;
      }
    .dashboard {
      margin-top: 0.5rem;
        transition: transform .25s ease;
      .dashboard-links {
      
      li{
        display:block;

        a{
          color:#625f6eec ;
          display:inline-block;
         // margin-top: 0.1rem;
       }
        svg{
       margin-right: 0.6rem;
       margin-left: 0.1rem;  
       font-size: 11px;
       height: 11px;
       width: 11px;
        
    } 
      }
       
    }
      a{
        width:100%;
         span:first-of-type{
             display:inline-block;
             font-size: 1rem;
              margin-left:10px;
              color: #565360;
             // margin-top: -5px;
           }
      .span1{
         width:25px;
         height:25px;
         display: inline-block;
         font-size: 0.8rem;
         line-height:1.5rem;
         text-align: center;
         color:#ff9f43;
         background:#ff9f431f;
         border-radius: 20px;
         margin-left:3rem;
       }
      .svg-icon{
          width:20px;
          position:absolute;
           bottom:-5px;
           left:0.6rem;
       }
      }
    }
li{
  a{
    width:100%;
    text-decoration: none;
    padding: 10px 15px ;
    color: #625f6e;
    line-height: 1.45;
  }
}   
}

.app_link {
        overflow:none;
         width:100%;
      li{
          color:#A6a4b0;
          font-size: 1rem;
          margin-bottom:1.3rem;
           width:100%;
         // background:blue;
         // margin-top: 1rem;
        .title{
          text-transform:uppercase;
          font-size: 0.9rem;
          margin-top: 1.5rem;
          display:inline-block;
          font-weight: 500;
          margin-left: 1rem;
          
        }
         a{
      //  background:red;
        width:100%;
        transition: transform .25s ease;
         line-height: 1.45;
         color: #625f6ee5 !important;
          .svg-icon{
          width:20px;
          position:absolute;
           bottom:-5px;
           left:7rem;
       }
      svg{
        margin-right: 0.9rem; 
        color:#565360 ;
        }
      }
     
      }
      a:hover{
        transform: translateX(5px) !important;
       // color:red !important;
      }

      .sub_links {
      li{
        padding:0;
        margin:0;
        
        a{
          color:#625f6eec ;
          display:inline-block;
          padding:10px 10px; 

         span{
          text-transform:capitalize;
          font-size: 1rem;
          display:inline-block;
          font-weight: 500;
          margin-left: 0.1rem;
          
        }
       }
        svg{
       margin-right: 0.6rem;
       margin-left: 0.1rem;  
       font-size: 11px;
       height: 11px;
       width: 11px;
        
    } 
      }
       
    }

     }
}

.sidenav-overlay{
  background-color: rgba(34,41,47,.5);
   position: fixed;
    top: 0;
    left: 0;
    right: 0;
    height: 120vh;
    z-index: 997;
    // display: block;
    // visibility: hidden;
    // opacity: 0;
    -webkit-transition: all .5s ease;
    transition: all .5s ease;
}
.show{
  display:block !important;
}
     ////////////////////////////////////////////////media 
@media screen and (max-width:950px) {
    .sidenav{
      display:none;
      .closetoggle{
        display:none !important;
      }
    }
    .navbar{
      width:94%;
      left:0px;
      .navbar-left{
        display:none !important;
      }
       .navbar-right{
           width:70% !important;
       }
       .toggle{
         display:block !important;
       }
    }
} 
@media screen and (max-width:700px) {
  .navbar{
    width:94%;
      left:-0.9rem;
  }
  .navbar-right{
      .dropdown{
        display:none;
      }
  }
  .hide{
     display:none;
  }
}
</style>