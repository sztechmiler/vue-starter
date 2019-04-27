<template>
<div>
	<label>Log in with mail</label> <input type="email" v-model="email">
	<button @click="enter()">{{buttonLabelToDisplay}}</button>
</div>
</template>

<script>
export default {
	props: ['buttonLabel'], 
 data() {
     return {
         email: 'Default Login from Form', 
         computed: 
         {
        	 buttonLabelToDisplay()
        	 {
        		 return this.buttonLabel || 'Zaloguj siê';  
        	 }
         }
     }
 },
 methods: {
     enter() {
         this.$emit('login', this.email);
     }
     
 }, 
 
 
 

}
</script>