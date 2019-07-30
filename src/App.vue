<template>
   <div id="app">
    <div class="header-bar right-content">
		<div class="container">
			<div class="skip-link screen-reader-text" href="#site-content">Skip to content</div>
			
<form role="search" method="get" class="search-form" action="http://mpbl.web.geniussports.com/">
	<label>
		<span class="screen-reader-text">Search for:</span>
		<input type="search" class="search-field" placeholder="Search" title="Press Enter to submit your search" value="" name="s">
	</label>
	<input type="submit" class="search-submit" value="Search">
</form>
								</div>
	</div>
  <div class="site-header-main">
		<div class="container">
			<div class="site-branding">
					<div class="custom-logo-container">
					<div class="custom-logo">
					<a href="http://mpbl.web.geniussports.com/" rel="home"></a>
					</div>
				  </div>
					<h2 class="site-title">
					<a href="http://mpbl.web.geniussports.com/" rel="home"><h2>Maharlika Pilipinas Basketball League</h2></a>
				  </h2>
											</div>

			<div class="header-social-logos">
        <section id="lab_social_icon_footer">
<!-- Include Font Awesome Stylesheet in Header -->
      <link href="//maxcdn.bootstrapcdn.com/font-awesome/4.1.0/css/font-awesome.min.css" rel="stylesheet">
      <div class="container">
      <div class="text-center center-block">
     </div>
     </div>
    </section>
							<ul class="social-customizer social-links footer-social-links">
									<li class="facebook-official">
						<a href="https://www.facebook.com/mpblofficialph/">
							<i class="fa fa-fw fa-facebook-square">
								<span>Facebook</span>
							</i>
						</a>
					</li>
									<li class="twitter">
						<a href="https://twitter.com/officialmpbl">
							<i class="fa fa-fw fa-twitter-square">
								<span>Twitter</span>
							</i>
						</a>
					</li>
									<li class="instagram">
						<a href="http://www.instagram.com/officialmpbl">
							<i class="fa fa-fw fa-instagram">
								<span>Instagram</span>
							</i>
						</a>
					</li>
								</ul>
						</div>
		</div>
	</div>
  <nav id="site-navigation" class="site-navigation" role="navigation">
		<span class="menu-toggle">Menu</span>
		<a class="skip-link screen-reader-text" href="#site-content">Skip to content</a>
		<div class="menu-main-menu-container">
      <ul id="menu-main-menu" class="menu">
        <li class="current-menu-item"><router-link to="/">Home</router-link></li>
          <li ><a href="/competitions/?cu=MPBL/schedule" title="Schedule">Schedule</a></li>
          <li ><a href="/competitions/?cu=MPBL/standings" title="Standings">Standings</a></li>
          <li ><a href="/competitions/?cu=MPBL/leaders" title="Leaders">Leaders</a></li>
           <li > <router-link to="/about">About</router-link></li>
          <li class="drop-menu">
          <a href="#" title="Menu">Menu</a>
          <ul class="sub-menu"></ul>
          </li></ul></div>	</nav>
          
    <router-view />
  </div>
</template>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}

body {
  font-family: 'Roboto', sans-serif;
}
.wrapper {
  width: 1500px;
  margin: auto;
  border: 1px solid #333;
}
.block {
  background-color: #F5F5F5;
  color: #008080;
  height: 100px;
  text-align: center;
  padding: 20px
}
.horizontal-scroll {
  background-color: rgb(138, 136, 136);
  overflow: hidden;
  overflow-x: scroll;
  overflow-y: hidden;
  white-space: nowrap;
  padding: 30px 0;
}
.item {
  border: 1px solid rgb(0, 0, 0);
  display: inline-block;
  width: 150px;
  background-color: rgb(5, 4, 4);
  text-align: center;
  padding: 50px 30px;
  font-size: 20px;
  margin: 0 10px
}
footer {
  color: #F5F5F5;
  text-align: left;
  background-color: #008080;
  padding: 20px;
  font-size: 12px;
}
.skip-link screen-reader-text{
  background-color: #42b983;
}

.fa {
  padding: 20px;
  font-size: 30px;
  width: 50px;
  text-align: center;
  text-decoration: none;
  margin: 5px 2px;
}

.fa:hover {
    opacity: 0.7;
}

.fa-facebook {
  background: rgb(20, 90, 243);
  color: white;
}
#lab_social_icon_footer {
  padding: 40px 0;
  background-color: #0955a0;
}

#lab_social_icon_footer a {
  color: #2c3e50;
}

#lab_social_icon_footer .social:hover {
  -webkit-transform: scale(1.1);
  -moz-transform: scale(1.1);
  -o-transform: scale(1.1);
}

#lab_social_icon_footer .social {
  -webkit-transform: scale(0.8);
  /* Browser Variations: */
  
  -moz-transform: scale(0.8);
  -o-transform: scale(0.8);
  -webkit-transition-duration: 0.5s;
  -moz-transition-duration: 0.5s;
  -o-transition-duration: 0.5s;
}
/*
    Multicoloured Hover Variations
*/

#lab_social_icon_footer #social-fb:hover {
  color: rgb(255, 255, 255);
}

#lab_social_icon_footer #social-tw:hover {
  color: rgb(255, 255, 255);
}

#lab_social_icon_footer #social-gp:hover {
  color: #d34836;
}

#lab_social_icon_footer #social-em:hover {
  color: #f39c12;
}
</style>
