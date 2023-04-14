<template>
	<div class="section">
		<div class="section__container">
			<div class="section__title">
				Cocok untuk Berbagai Jenis & Skala Bisnis
			</div>
			<div class="section__desc">
				Semua layanan LummoSHOP mendukungmu yang baru memulai, sudah merintis ataupun sedang ingin membesarkan bisnis.
			</div>
		</div>
		<div class="carousel__container">
			<Carousel :autoplay="5000" v-bind="settings" :breakpoints="breakpoints">
				<Slide v-for="slide in slides" :key="slide">
					<div class="image__container">
						<img :src="slide.url" class="shops__image" />
						<div class="shops__container">
							<div>
								<img :src="slide.iconUrl" class="icons__image" />
							</div>
							<div class="shops__text">
								<div class="shop__name">{{ slide.shopName }}</div>
								<div class="shop__type">{{ slide.shopType }}</div>
							</div>
						</div>
					</div>
				</Slide>

				<template #addons>
					<Navigation />
				</template>
			</Carousel>
		</div>
	</div>
</template>

<script setup>
import { Carousel, Navigation, Slide } from 'vue3-carousel'
import 'vue3-carousel/dist/carousel.css';

const settings = ({
	itemsToShow: 1,
	snapAlign: 'center',
});

const breakpoints = ({
	// 700px and up
	700: {
		itemsToShow: 2,
		snapAlign: 'center',
	},
	// 1024 and up
	1024: {
		itemsToShow: 3,
		snapAlign: 'start',
	},
	1400: {
		itemsToShow: 4,
		snapAlign: 'start',
	},
});

const slides = (
	[
		{
			url: "https://lummoshop.co.id/wp-content/uploads/2022/01/vr_tjendol.png",
			shopName: "TSDC Store",
			iconUrl: 'https://lummoshop.co.id/wp-content/uploads/2022/01/logo-store-5.jpg',
			shopType: 'Pakaian'
		},
		{
			url: "https://lummoshop.co.id/wp-content/uploads/2022/01/petite-bakery.png",
			shopName: "TSDC Store",
			iconUrl: 'https://lummoshop.co.id/wp-content/uploads/2022/01/logo-store-5.jpg',
			shopType: 'Pakaian'
		},
		{
			url: "https://www.lummoshop.co.id/wp-content/uploads/2022/02/wannabe-19-mockup-810p-1650p.png",
			shopName: "TSDC Store",
			iconUrl: 'https://lummoshop.co.id/wp-content/uploads/2022/01/logo-store-5.jpg',
			shopType: 'Pakaian'
		},
		{
			url: "https://www.lummoshop.co.id/wp-content/uploads/2022/02/wesafeu-mockup-810p-1650p.png",
			shopName: "TSDC Store",
			iconUrl: 'https://lummoshop.co.id/wp-content/uploads/2022/01/logo-store-5.jpg',
			shopType: 'Pakaian'
		},
		{
			url: "https://lummoshop.co.id/wp-content/uploads/2022/01/mookie.png",
			shopName: "TSDC Store",
			iconUrl: 'https://lummoshop.co.id/wp-content/uploads/2022/01/logo-store-5.jpg',
			shopType: 'Pakaian'
		},
		{
			url: "https://www.lummoshop.co.id/wp-content/uploads/2022/02/ardana-shop-mockup-810p-1650p.png",
			shopName: "TSDC Store",
			iconUrl: 'https://lummoshop.co.id/wp-content/uploads/2022/01/logo-store-5.jpg',
			shopType: 'Pakaian'
		},
		{
			url: "https://www.lummoshop.co.id/wp-content/uploads/2022/02/dansa-shop-mockup-810p-1650p.png",
			shopName: "TSDC Store",
			iconUrl: 'https://lummoshop.co.id/wp-content/uploads/2022/01/logo-store-5.jpg',
			shopType: 'Pakaian'
		},
		{
			url: "https://www.lummoshop.co.id/wp-content/uploads/2022/02/wesafeu-mockup-810p-1650p.png",
			shopName: "TSDC Store",
			iconUrl: 'https://lummoshop.co.id/wp-content/uploads/2022/01/logo-store-5.jpg',
			shopType: 'Pakaian'
		},
		{
			url: "https://lummoshop.co.id/wp-content/uploads/2022/01/m-3.png",
			shopName: "TSDC Store",
			iconUrl: 'https://lummoshop.co.id/wp-content/uploads/2022/01/logo-store-5.jpg',
			shopType: 'Pakaian'
		}
	]
)
</script>

<style scoped>
.section {
	padding: 100px 0;
	background-color: var(--project-blue) !important;
}
.section__container {
	max-width: 775px;
	margin-left: auto;
	margin-right: auto;
	text-align: center;
	font-weight: 500;
	padding-bottom: 20px;
	font-weight: 600;
}
.section__title {
	font-size: 2.25rem;
	line-height: 2.5rem;
	color: #ffffff;
}
.section__desc {
	font-size: 16px;
	color: #ADA4D3;
	margin-top: var(--spacing-4);
}
.image__container {
  display: flex;
	flex-direction: column;
  align-items: center;
  width: 260px;
	height: 600px;
}

.shops__image {
	width: inherit;
	height: inherit;
}

.shops__container {
	display: flex;
	align-items: center;
	width: inherit;
	justify-content: left;
	margin-top: var(--spacing-4);
}

.shops__text {
	color: var(--white);
	margin-left: var(--spacing-2);
	display: flex;
	flex-direction: column;
	align-items: baseline;
}

.shop__type {
	color: #ada4d3;
	font-size: 0.875rem;
	line-height: 1.125rem;
	font-weight: 400;
	margin-bottom: 0;
}
.icons__image {
	width: 42px;
	border-radius: 100%;
}

.carousel__container {
	max-width: 1400px;
	margin: auto;
}

@media screen and (max-width: 950px) {
	.section__title {
		font-size: 1.5rem;
		line-height: 2.125rem;
	}
	.section__desc {
		font-size: 14px;
	}
	.section__container {
		padding: var(--spacing-4);
	}
}
</style>