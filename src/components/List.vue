<template>
	<section class="listItems mt-5">
		<div class="container">
			<div class="row mt-2 p-3 shadow p-3" v-for="(item) in items"  :key="item.id" exact>
				<div class="col-lg-3">
					<img :src="item.imgUrl" :alt="item.altImg">
				</div>
				<div class="col-lg-5 border-start border-dark relative">
					<h5>{{item.title}}</h5>
					<p>{{item.text}}</p>
					<button type="button" class="btn btn-dark mt-4 ">Dark</button>
				</div>
			</div>
		</div>
	</section>
</template>

<script>
export default {
	data() {
		return {
			items: [
				{
					id: 1,
					imgUrl:  require('../assets/images/slider/1.jpg'),
					altImg: "some",
					title: "title",
					text:  "Lorem lorem lorem lorem Lorem lorem lorem lorem Lorem lorem lorem lorem Lorem lorem lorem lorem Lorem lorem lorem lorem",
					link: "https://yummyanime.club/catalog/item/tvoya-aprel-skaya-lozh"
				},
				{
					id: 2,
					imgUrl:  require('../assets/images/slider/2.png'),
					altImg: "some",
					title: "title",
					text:  "Lorem lorem lorem lorem Lorem lorem lorem lorem Lorem lorem lorem lorem Lorem lorem lorem lorem Lorem lorem lorem lorem",
					link: "https://yummyanime.club/catalog/item/tvoya-aprel-skaya-lozh"
				},
				{
					id: 3,
					imgUrl:  require('../assets/images/slider/3.png'),
					altImg: "some",
					title: "title",
					text:  "Lorem lorem lorem lorem Lorem lorem lorem lorem Lorem lorem lorem lorem Lorem lorem lorem lorem Lorem lorem lorem lorem",
					link: "https://yummyanime.club/catalog/item/tvoya-aprel-skaya-lozh"
				},
				{
					id: 4,
					imgUrl:  require('../assets/images/slider/1.jpg'),
					altImg: "some",
					title: "title",
					text:  "Lorem lorem lorem lorem Lorem lorem lorem lorem Lorem lorem lorem lorem Lorem lorem lorem lorem Lorem lorem lorem lorem",
					link: "https://yummyanime.club/catalog/item/tvoya-aprel-skaya-lozh"
				},
				{
					id: 5,
					imgUrl:  require('../assets/images/slider/1.jpg'),
					altImg: "some",
					title: "title",
					text:  "Lorem lorem lorem lorem Lorem lorem lorem lorem Lorem lorem lorem lorem Lorem lorem lorem lorem Lorem lorem lorem lorem",
					link: "https://yummyanime.club/catalog/item/tvoya-aprel-skaya-lozh"
				}

			],
			popularItems: [
				{
					id: 1,
					imgUrl:  require('../assets/images/slider/2.png'),
					alt: "some",
					title: "title",
					link: "https://yummyanime.club/catalog/item/tvoya-aprel-skaya-lozh"
				},
				{
					id: 2,
					imgUrl:  require('../assets/images/slider/1.png'),
					alt: "some",
					title: "title",
					link: "https://yummyanime.club/catalog/item/tvoya-aprel-skaya-lozh"
				},
				{
					id: 3,
					imgUrl:  require('../assets/images/slider/3.png'),
					alt: "some",
					title: "title",
					link: "https://yummyanime.club/catalog/item/tvoya-aprel-skaya-lozh"
				},
				{
					id: 4,
					imgUrl:  require('../assets/images/slider/2.png'),
					alt: "some",
					title: "title",
					link: "https://yummyanime.club/catalog/item/tvoya-aprel-skaya-lozh"
				},
				{
					id: 5,
					imgUrl:  require('../assets/images/slider/2.png'),
					alt: "some",
					title: "title",
					link: "https://yummyanime.club/catalog/item/tvoya-aprel-skaya-lozh"
				}
			]
		};
	},
};
</script>


<style lang="scss" scoped>
	img {
		display: block;
		width: 100%;
		height: auto;
	}
	.btn {
		position: absolute;
		bottom: 0;
		width: 20%;
	}
	.relative {
		position: relative;
	}
	p {
		margin-bottom: 4rem;
	}
	.listItems {
		position: relative;
		&__popularItem {
			display: flex;
			width: 100%;
			position: relative;
			margin-top: 1rem;
		}
		&__popularImage {
			width: 100%;
			position: relative;
			img {
				display: block;
				width: 100%;
				height: auto;
			}
		}
		&__popularTitle {
			text-align: center;
			width: 100%;
		}
	}
	.popular {
		border: 1px solid black;
		width: 100%;
	}
</style>

