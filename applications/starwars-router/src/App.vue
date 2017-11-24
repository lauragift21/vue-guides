<template>
	<div id="app">
		<h3>StarWars Router</h3>	
		<h4>
			<router-link to="/people">Meet the Charaters</router-link>
			<router-link to="/planets">Visit the Planets</router-link>
		</h4>	
		<router-view></router-view>
	</div>
		
</template>

<script>
export default {
	name: 'app',
	data() {
	  return {
	  	title: 'Random Name Router'
	  }
	}
}
	
</script>