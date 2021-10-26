<template>
	<div id="carouselExampleControls" class="carousel slide" data-bs-ride="carousel">
  <div class="carousel-inner">
    <div class="carousel-item" v-for="(slide, index) in slides" :key="slide.id" :class="{'active' : index === 0}" exact >
      <img :src="slide.url" class="d-block w-100 carousel__img" :alt="slide.alt">
		<div class="carousel-caption d-none d-md-block">
			<h5>{{slide.title}}</h5>
			<p>Some representative placeholder content for the third slide.</p>
			</div>
    </div>
  </div>
  <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleControls" data-bs-slide="prev">
    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
    <span class="visually-hidden">Previous</span>
  </button>
  <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleControls" data-bs-slide="next">
    <span class="carousel-control-next-icon" aria-hidden="true"></span>
    <span class="visually-hidden">Next</span>
  </button>
</div>
</template>


<style lang="scss" scoped>
	.carousel{
		margin-top: 3rem; 
	}
</style>


<script>
export default {
	data() {
		return {
			slides: [
				{
					id: 1,
					alt: "The A - Z Guide Of WAR",
					url:  require('../assets/images/slider/1.jpg'),
					title: "Beware The ANIME Scam",

				},
				{
					id: 2,
					alt: "some",
					url:  require('../assets/images/slider/2.png'),
					title: "The Secrets To GATE",

				},
				{
					id: 3,
					alt: "GATE Adventures",
					url:  require('../assets/images/slider/3.jpg'),
					title: "GATE Adventures",

				},
				{
					id: 4,
					alt: "Get Rid of BI For Good",
					url:  require('../assets/images/slider/4.png'),
					title: "Get Rid of BI For Good",

				}
			]
		}
	},
}
</script>
<style lang="scss" scoped>
	.carousel {

	}
	.carousel-item {
		&:hover {
			.carousel-caption {
				opacity: 1;
			}
		}
	}
	.carousel-caption {
		transition: 0.3s all;
		background-color: #212529f5;
		width: 100%;
		left: 0;
		bottom: 0;
		opacity: 0;
	}
</style>