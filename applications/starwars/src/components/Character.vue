<template>
	<div class="col-md-4" @click="switchCharacter">
		<div class="character-card">
			<div class="card-block">
				<p class="card-title">Surname: {{character.surname}}</p>				
				<p class="card-title">Name: {{character.name}}</p>				
				<p class="card-text">Gender: {{character.gender}}</p>				
				<p class="card-text">Country: {{character.region}}</p>				
			</div>
		</div>
	</div>
	
</template>

<script>

export default {
	props: ['name'],
	data() {
		return {
			character: {}
		}
	},
	methods: {
		fetchCharater() {
			fetch(`https://uinames.com/api/?ext/${name}`, {
				method: 'GET'
			})
			.then(response => response.json())
			.then(json => this.character = json)
		},
		switchCharacter() {
			let random_name = Math.floor(Math.random() * 300) + 1
			this.fetchCharater(random_name)
		}
	},
	created () {
		this.fetchCharater(this.name)
	}
}
	
</script>