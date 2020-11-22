<template>
<div id="dashboard">
    <header>
      <div v-if="isElVisible" id="user_subscription_plan_pro"> 
        <h1 id="user_subscription_plan_button_pro">UnApp Pro</h1>
      </div>
      <div v-else id="user_subscription_plan"> 
        <h1 id="user_subscription_plan_button">UnApp Basic</h1>
      </div>
      <div id="user_info">
        <select id="select_language"><!-- languages -->
            <option value="eng">English</option>
            <option value="rus">Russian</option>
            <option value="kaz">Kazakh</option>
        </select> 
        <div id="user_button"> <!-- user -->
          <img src="./assets/user.png" alt="">
        </div>
      </div>
    </header>
    <div id="dropdown_menu" v-if="hover">
            <div><img src="./assets/dropdown_menu_icons/user_drp.png" alt=""><a href="">Profile</a></div>
            <div><img src="./assets/dropdown_menu_icons/gear.png" alt=""><a href="">Settings</a></div>
            <div><img src="./assets/dropdown_menu_icons/feedback.png" alt=""><a href="">Leave a feedback</a></div>
            <div><img src="./assets/dropdown_menu_icons/rocket.png" alt=""><a href="">UnApp Pro</a></div>
            <hr id="dropdown_menu_divider" align="center" width="100%" size="50" color="#dddddd" />
            <div id="drp_lastchild"><img src="./assets/dropdown_menu_icons/logout.png" alt=""><a href="">Log Out</a></div>
    </div>
    <div id="main">
      <div id="cont">
        <div id="main_first_block">
          <div id="main_heading">
           <h1>Find out everything you need to apply to the best universities in the world</h1>
            <p>Video courses and webinars from practicing students of the best universities in the world</p>
          </div>
          <div id="main_button">Buy UnApp Pro</div>
        </div>
        <div id="main_second_block">
          <img src="./assets/mainric_removebg.png" alt="">
        </div>
      </div>
    </div>
    <div id="courses_section"> 
      <h1 id="popular_c">Popular Courses</h1>
      <div id="all_courses">
        <div id="course_block">
          <div id="course_cover" class="course_cover_one">
            <div id="unapppro_course"></div>
          </div>
          <h5>Applying to US Universities</h5><!-- название курса -->
          <p>Yerkebulan Imanbaev</p><!-- ведущий курса -->
          <h6>Language: Russian</h6>
        </div>
        <div id="course_block">
          <div id="course_cover" class="course_cover_two">
            <div id="unapppro_course"></div>
          </div>
          <h5>Как продать себя университету?</h5><!-- название курса -->
          <p>Aidana Smat</p><!-- ведущий курса -->
          <h6>Language: Russian</h6>
        </div>
        <div id="course_block">
          <div id="course_cover" class="course_cover_three">
            <div id="unapppro_course"></div>
          </div>
          <h5>Рекомендательные письма для чайников</h5><!-- название курса -->
          <p>UnApp Team</p><!-- ведущий курса -->
          <h6>Language: Russian</h6>
        </div>
        <div id="course_block">
          <div id="course_cover" class="course_cover_four">
            <div id="unapppro_course"></div>
          </div>
          <h5>Как поступить во Францию?</h5><!-- название курса -->
          <p>Medina Sovetova</p><!-- ведущий курса -->
          <h6>Language: Russian</h6>
        </div>
        <div id="course_block">
          <div id="course_cover" class="course_cover_five">
            <div id="unapppro_course"></div>
          </div>
          <h5>Поступление в университеты Южной Кореи</h5><!-- название курса -->
          <p>Azhar Kamerdenova</p><!-- ведущий курса -->
          <h6>Language: Russian</h6>
        </div>
      </div>
    </div>
</div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return{
      
      isElVisible: true, // если true то меняется на Unapp pro
      hover: false,
      user:{
        id:1,
        email:'someone@gmail.com',
        hasSubscription: false,
      }
    }
  }
}
</script>

<style>
template{
  background: #eaeaea;
}
header{
  widows: 100%;
  height: 60px;
  display: block;
}
#user_subscription_plan{
  height: 50%;
  width: 90px;
  text-align: center;
  border-radius: 5px 5px 5px 5px;
  display: table;
  float: left;
  background: #db7920;
  position: relative;
  top: 20%;
  left: 100px;
}
#user_subscription_plan_pro{
  height: 50%;
  width: 90px;
  text-align: center;
  border-radius: 5px 5px 5px 5px;
  display: table;
  float: left;
  background: rgb(62, 33, 121);;
  position: relative;
  top: 20%;
  left: 100px;
}
#user_subscription_plan_button {
  color: white;
  font-size: 13px;
  height: 100%;
  
  vertical-align: middle;
  display: table-cell;
}
#user_subscription_plan_button_pro{
  color: white;
  font-size: 13px;
  height: 100%;
  
  vertical-align: middle;
  display: table-cell;
}
#user_info{
  width:200px;
  display: flex;
  justify-content: space-around;
  align-items: center;
  height: 60%;
  text-align: center;
  float: right;
position: relative;
  top: 20%;
  right: 100px;
}
#user_button{
  width: 45px!important;
  height:45px;
  display: flex;
  justify-content: space-around;
  align-items: center;
  background: #fa5059;
  border-radius: 50%;
}
#user_button:hover {
  cursor: pointer;
}
#select_language{
  width: 100px;;
  height: 30px;;
  padding-right: -15px;
  padding-left: 5px;
  background: white;
  border-radius: 0.1px solid black;
  opacity: 0.9;
  border-radius: 3px 3px 3px 3px;
}
#dropdown_menu{
  padding-top: 7px;;
width:155px;
height: 190px;;
color: black;
  border-radius: 5px 5px 5px 5px;
  position:absolute;
  background:#fff;
  float: right!important;
  box-shadow: 0px 0px 10px ;
  font-size: 14px;;
  display: none;
  z-index: 1;
}
#dropdown_menu div {
  padding-top: 6px;
padding-left: 8px;;
}
#dropdown_menu a {
  color: black;
  text-decoration: none;
  padding-left: 6px;;
}
#dropdown_menu img {
  position: relative;
  top: -2px;;
}
#dropdown_menu div:hover{
  background:#c99691;
  transition: 0.2s;
  cursor: pointer;
}
/* #dropdown_menu_divider{
  width:100%;
  height: 1px;
  background: #000;;
  opacity: 0.2;;
  margin-top: 7px;
  margin-bottom: 7px;
} */

/* main block */

#main{
  width:100%;
  height: 450px;;
  margin-top: 20px;;
}
#cont{
  width: 90%;
  margin: 0 auto;
  background: rgb(62, 33, 121) ;
  height: 100%;;
  border-radius: 10px 10px 10px 10px;
  color: #fff;
}
#main_first_block{
  width:55%;
  position: relative;
  top: 15%;
  left: 50px;;
}
#main_heading p{
  padding-top: 10px;;
  font-size: 20px;;
}
#main_button{
  width:150px;
  height: 45px;;
  background: #fa5059;
  text-align: center;
  border-radius: 10px 10px 10px 10px;
  display: flex;
  justify-content: center;
  align-items: center;
  position: relative;
  top: 20px;;
}
#main_button:hover{
  cursor: pointer;
  background: #f89398;
  transition: 0.4s; ;
}
#main_second_block{
  width:45%;
  float: right;
  position: relative;
  top: -300px;; 
  left: 35px;;
}
#main_second_block img{
  width:95%;
}


/* courses */
#courses_section{
  width:100%;
  height: 600px;
  margin-top: 60px;
}
#popular_c{
  width: 90%;
  margin: 0 auto;
}
#all_courses{
  position: relative;
  top: -100px;
  width:90%;
  margin: 0 auto;
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-auto-rows: 330px;
  grid-column-gap: 30px;
   grid-row-gap: 3em;
}
#course_block{
  /* width: 350px; */
      box-shadow: rgba(0, 0, 0, 0.1) 0px 0px 10px;
  border-radius: 10px 10px 10px 10px;
  
}
#course_block:hover{
  transition: 0.5s;;
  transform: scale(1.1);
  cursor: pointer;
}
#course_cover{
  width: 100%;
  height: 190px;
  border-radius: 10px 10px 10px 10px;
}
.course_cover_one{
  background: rgb(235, 97, 52);
}
.course_cover_two{
  background: rgb(
95, 217, 103
);
}
.course_cover_three{
  background: rgb(126, 199, 228);
}
.course_cover_four{
  background: rgb(233, 135, 156);
}
.course_cover_five{
  background: rgb(207, 121, 241);
}
#course_block h5 {
  width: 98%;
  padding-left: 15px;
  padding-top: 5px;
  font-size: 18px;;
}
#course_block p {
  padding-left: 15px;
  opacity: 0.8;
  margin-top: -5px!important;
}
#course_block h6{
  padding-left: 15px;
}
</style>
