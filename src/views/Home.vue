<template>
	<section class="home" >
		<SliderFull class="slider" />
		<div class="container containerDark">
			<h2  class="text-center mt-5">Fresh chapters</h2>
			<List/>
		</div>
	</section>
</template>

<style lang="scss" scoped>
	.home {
		position: relative;
		width: 100%;
		height: 100vh;
	}
	.containerDark {
		background-color: #212529;
	}
	.slider  {
		margin-top: 4rem;
	}
</style>

<script>

import List from '@/components/List.vue';
import SliderFull from '@/components/SliderFull.vue';

export default {
	name: 'Home',
	components: {
		List, SliderFull
	}
}
</script>