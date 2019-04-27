<template>
<div id="app">
	<img alt="Vue logo" src="./assets/logo.png">
	<HelloWorld msg="Welcome to Your Vue.js App" />
	<h1>Welcome in class enrollment system </h1>
	<p>Log in with e-mail 
		<input v-model="email" type="text">
		<button @moseover="login()">log in</button>
		
	</p>
	
</div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default 
{
  	name: 'app',
  	components: 
  	{
    	HelloWorld
	},
	
	data()
	{
		  return {
			  email: 'moj mail',
			  password: ''		  
		  		};		  
	},
	methods: {
		alertMyEmail(){
			alert(this.email);
		},
		login(){
			email: ''
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
