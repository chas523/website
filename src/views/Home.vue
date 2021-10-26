<template>
	<section class="home" >
		<SliderFull class="slider" />
		<div class="container">
			<div class="row">
				<h1 class="home__title">Popular today</h1>
			</div>
			<div class="row">
				<div class="col-lg-6">
					<CarouselBootstrap />
				</div>
				<div class="col-lg-6">
					<Card />
				</div>
			</div>
			<div class="row mt-5">
				<div class="col-lg-6">
					<p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Eveniet nisi veritatis iure ab facilis assumenda odit dolores, unde rem rerum aliquam praesentium facere voluptas provident aliquid quibusdam hic dolore inventore? Lorem ipsum dolor sit amet consectetur adipisicing elit. Fugiat expedita at dolorum, totam, perferendis sunt odit earum quasi laborum cumque ipsa asperiores obcaecati nam? Culpa facilis hic dicta iure magnam.</p>
				</div>
				<div class="col-lg-6">
				</div>
			</div>
			<List />
		</div>
	</section>
</template>

<style lang="scss" scoped>
	.home {
		position: relative;
		width: 100%;
		&__title {
			margin-top: 4rem;
			font-size: 24px;
			text-transform: capitalize;
		}
	}
	.containerDark {
		background-color: #212529;
	}
	.slider  {
		margin-top: 4rem;
	}
	.card {
		margin-top: 49px;
	}
</style>

<script>

import SliderFull from '@/components/SliderFull.vue';
import CarouselBootstrap from '@/components/CarouselBootstrap.vue'
import Card  from '@/components/Card.vue';
import List from '@/components/List.vue';

export default {
	name: 'Home',
	components: {
		SliderFull,
		CarouselBootstrap,
		Card,
		List
	}
}
</script>