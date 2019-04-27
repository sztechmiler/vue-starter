<template>
<div id="app">
	<img alt="Vue logo" src="./assets/logo.png">
	<!--  <HelloWorld msg="Welcome to Your Vue.js App" />-->
	<h1>Welcome in class enrollment system </h1>
	
	<p v-if="logged==true">Log in with e-mail 
		<input v-model="email" type="text">
		<button @click="login()">log in</button>
		
	</p>
	<p v-else="logged-false">Witaj {{email}} !
	<button @click="login()"> log out</button>
	
	</p>
	
</div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';
import "milligram";
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
			  email: 'Default mail',
			  password: '',
			  logged: true
		  		};		  
	},
	methods: {
		alertMyEmail(){
			alert(this.email);
		},
		login(){
			if(this.logged){
			this.logged= false
			}
			else{
				this.logged= true
			}
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
