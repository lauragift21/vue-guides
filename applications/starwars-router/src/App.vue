<template>
	<div id="app">
		<h3>StarWars Router</h3>	
		<h4>
			<router-link class="link" to="/data/people">Meet the Charaters</router-link> |
			<router-link class="link" to="/data/planets">Explore the Planets</router-link>
		</h4>	
		<router-view></router-view>
	</div>	
</template>