<template>
	<div id="app">
		<h3>{{title}}</h3>
		<div class="col-md-12">
		<Character 
			v-for="(name,index) in initials_id"	
			:id="1"
			:key="index"
		/>
			
		</div>
	</div>
</template>

<script>
import Character from './components/Character.vue';
	export default {
		name: 'app',
		data() {
		  return {
		    title: 'Random Names',
		    initials_id: [1,2,3,4,5]
		  }
		},
		components: {
			Character
		}
	}
</script>

