<template>
   <div id="app">
  <div class="hello">
    <h1>{{ msg }}</h1>
  <div id="app">
    <div class="home">
        <div class="standings"><h1>STANDINGS</h1>
          <div class="post" v-for="post in posts" :key="post.id">
          <div class="scorePerGame" >
            <table class="table table-dark">
              <thead>
                <tr>
                  <th scope="col" class="font">ID</th>
                  <th scope="col"  class="font">Team</th>
                  <th scope="col" class="font"></th>
                  <th scope="col" class="font">Win</th>
                  <th scope="col" class="font">Lose</th>
                  <th scope="col" class="font" >Location</th>
                  <th scope="col" class="font">Team Leader</th>
                  <th scope="col" class="font">Team Manager</th>

                </tr>
              </thead>
              <tbody>
                <tr v-for="p in post.data" :key="p.id">
                  <th class="align"> {{p.id}}</th>
                  <td class="align"><img :src="p.image.url" width="100%" v-if="p.image.url" /></td>
                  <td class="align">{{p.name}}</td>
                  <td class="align">{{p.win}}</td>
                  <td class="align">{{p.lose}}</td>
                  <td class="align">{{p.location_preference}}</td>
                  <td class="align">{{p.team_leader}}</td>
                  <td class="align">{{p.team_manager}}</td>
                </tr>
              </tbody>
            </table>

          </div>
        </div>
  </div>
  </div>
  </div>
  <nav id="site-navigation" class="site-navigation" role="navigation">
		<!-- <span class="menu-toggle">Menu</span> -->
		<a class="skip-link screen-reader-text" href="#site-content">Skip to content</a>
		<div class="menu-main-menu-container">
      <ul id="menu-main-menu" class="menu">
        <!-- <li class="current-menu-item"></li> -->
          <li ><a href="/competitions/?cu=MPBL/schedule" title="Schedule">SCHEDULE</a></li>
          <li ><a href="/competitions/?cu=MPBL/standings" title="Standings">STANDINGS</a></li>
          <li ><a href="/competitions/?cu=MPBL/leaders" title="Leaders">LEADERS</a></li>
          <li ><a href="/competitions/?cu=MPBL/statistics" title="statistics">STATISTICS</a></li>
          <li ><a href="/competitions/?cu=MPBL/teams" title="teams">TEAMS</a></li>
          <li ><a href="/competitions/?cu=MPBL/players" title="players">PLAYERS</a></li>

          <!-- <li class="drop-menu">
          <a href="#" title="Menu">Menu</a>
          <ul class="sub-menu"></ul> -->
          </li></ul></div>	</nav>
        <section class="block">This is a content</section>
        <footer id="site-footer" class="site-footer footer-layout-1" role="contentinfo">
        <div class="container">
        <div class="site-info">
        <span class="site-copyright">&copy; Genius Sports Group. All content responsibility of site administrator.</span>
        <span class="global-logo">
        <a title="Genius Sports Group" href="http://geniussports.com/">
            Genius Sports Group
        </a>
        </span>
        </div>
        </div>
        </footer>	
        </div>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";
import axios from 'axios'
export default {
  data(){
    return{
      posts:[]
    }
  },

  mounted(){
    var self = this;
    axios.get('http://api.crossovrapp.com/v3/mpbl/teams')
    .then(function(res){
      self.posts =  res.data;
      console.log('Data:', res.data);
  })
  .catch(function(error){
    console.log('Error: ', error);
  })
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#app {
  font-family:'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: #2c3e50;
  background: #f8f6f6;
}
#nav {
  padding: px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}

.post {
  background-color: rgb(253, 252, 252);
   text-align: left;
  width: 600px;
  height: 400px;
}
.scorePerGame {
  background-color: rgb(221, 221, 221);
  margin: 50px;
  width: 500px;
  border-style: dotted;
 text-align: center;
}
.standings{
   margin: 60px;
   color: rgb(122, 122, 122);
   font-family:Georgia, 'Times New Roman', Times, serif;
   font-style:Bold;

}
.align{
  text-align: center;
  border-radius: 8px;
  font-size: 13px;
}
.font{
    font-size: 13px;
    font-style: Bold;
}
.block{
  background: #c4c4c4;
}
</style>
