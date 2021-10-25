<template>
	<swiper class="swiper shadow p-3" :options="swiperOption">
		<swiper-slide v-for="slide in slides" :key="slide.id" >
			<div class="swiper__wrapper">
				<div class="swiper__img">
					<img :src="slide.url" alt="" class="rounded">
					<div class="swiper__likes rounded shadow p-1">&nbsp;&hearts;&nbsp;&nbsp;&nbsp;{{slide.likes}}</div>
				</div>
				<a class="swiper__title" href="#">{{slide.title}}</a>
				<div class="swiper__tag text-secondary"> {{slide.tag}}</div>
			</div>
		</swiper-slide>
	</swiper>
</template>

<script>
import { Swiper, SwiperSlide } from 'vue-awesome-swiper';
import 'swiper/css/swiper.css';

export default {
	components: {
		Swiper,
		SwiperSlide,
	},
	data() {
		return {
			swiperOption: {
				slidesPerView: 1,
				spaceBetween: 30,
				loop: true,
				autoplay: {
					delay: 2500,
					disableOnInteraction: false
				},
				breakpoints: {
					1200: {
						slidesPerView: 6,
					}
				}
			},
			slides: [
				{
					id: 1,
					alt: "The A - Z Guide Of WAR",
					url:  require('../assets/images/slider/1.jpg'),
					title: "Beware The ANIME Scam",
					tag: "genre",
					likes: 200,
				},
				{
					id: 2,
					alt: "some",
					url:  require('../assets/images/slider/2.png'),
					title: "The Secrets To GATE",
					tag: "genre",
					likes: 220,
				},
				{
					id: 3,
					alt: "GATE Adventures",
					url:  require('../assets/images/slider/3.jpg'),
					title: "GATE Adventures",
					tag: "genre",
					likes: 400,
				},
				{
					id: 4,
					alt: "Get Rid of BI For Good",
					url:  require('../assets/images/slider/4.png'),
					title: "Get Rid of BI For Good",
					tag: "genre",
					likes: 192,
				},
				{
					id: 5,
					alt: "some",
					url:  require('../assets/images/slider/1.png'),
					title: "The A - Z Guide Of WAR",
					tag: "genre",
					likes: 122,
				},
				{
					id: 6,
					alt: "some",
					url:  require('../assets/images/slider/5.png'),
					title: "title",
					tag: "genre",
					likes: 192,
				},
				{
					id: 7,
					alt: "some",
					url:  require('../assets/images/slider/6.png'),
					title: "title",
					tag: "genre",
					likes: 192,
				},
			],
		};
	},
};
</script>

<style lang="scss" scoped>
	.swiper {
		&__wrapper {
			position: relative;
			width: 100%;
			height: auto;
			img {
				display: block;
				width: 100%;
				height: auto
			}
		}
		&__img  {
			position: relative;
			width: 100%;
			height: auto;
		}
		&__title {
			margin-top: 10px;
			display: block;
			text-decoration: none;
			color: #fff;
			font-size: 20px;
			&:hover {
				color: #fff;
			}
		}
		&__likes {
			position: absolute;
			bottom: 10px;
			left: 10px;
			background-color: rgba(0, 0, 0, 0.63);
			width: 70px;

		}

	}

</style>