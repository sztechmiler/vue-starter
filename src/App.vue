<template>
<div id="app">
	<img alt="Vue logo" src="./assets/logo.png">
	<h1>Welcome in class enrollment system </h1>
	
	<div v-if="isAuthenticated">
		Hello {{authenticatedUsername}}
	</div>
	<div v-else>
		<login-form @login="logMeIn($event)" ></login-form>
	</div>
</div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';
import "milligram";
import LoginForm from './LoginForm.vue';
export default 
{
  	name: 'app',
  	components: 
  	{
    	HelloWorld, 
    	LoginForm
	},
	
	data()
	{
		  return {
			password: '',
			logged: true, 
			authenticatedUsername: '',
			isAuthenticated: false
		  		};		  
	},
	methods: {
		alertMyEmail(){
			alert(this.email);
		},
		login(){
				this.isAuthenticated= true
				},
			
		logMeIn(username) {
			  this.authenticatedUsername = username;
			  this.login();
			}
	}
}


</script>

<style>
#app {
	font-family: 'Avenir', Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	text-align: center;
	color: #2c3e50;
	margin-top: 60px;
}
</style>
