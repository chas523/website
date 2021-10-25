<template>
	<header class="header fixed-top">
	<nav class="navbar navbar-expand-lg  navbar-dark bg-dark">
  <div class="container">
    <a class="navbar-brand" href="#">Your logo</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
		<div class="navbar-nav">
			<router-link v-for="item in items" :key="item.id" :to="item.url" class="nav-link " exact>{{item.text}}</router-link>
		</div>
	</div>
  </div>
</nav>
	</header>
</template>

<script>
export default ({
	data() {
		return  {
			items: [
				{
					id: 1,
					text: 'Home',
					url: '/'
				},
				{
					id: 2,
					text: 'About',
					url: '/about'
				},
				{
					id: 3,
					text: 'Typography',
					url: '/typography'
				},
				{
					id: 4,
					text: 'Contacts',
					url: '/contacts'
				}
			]
		}
	}
})
</script>

<style lang="scss" >

</style>

