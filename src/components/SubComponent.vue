<template>
	<div class="section">
		<div class="section__container">
			<div class="section__title">
				Banyak Fitur Toko Online Pintar untuk Kendalikan Bisnis Lebih Mudah
			</div>
			<div class="section__desc">
				Kamu bisa gunakan fitur-fitur toko online yang saling terhubung untuk membuat proses bisnis-mu lebih simpel, efisien, dan akurat.
			</div>
		</div>
		<BodyFeature
      titleText="Website Toko Online yang Mudah Dikelola"
      titleDesc="Pengelolaan bisnis semakin praktis dengan sistem manajemen order, pembayaran, hingga pengiriman barang yang lengkap."
      imageUrl="https://lummoshop.co.id/wp-content/uploads/2022/01/image-1.png"
      flexDirection="row"
    />
		<BodyFeature
      titleText="Produk-mu Jadi Pusat Perhatian"
      titleDesc="Tanpa saingan & perang harga, pengunjung lebih terpikat untuk membeli."
      imageUrl="https://lummoshop.co.id/wp-content/uploads/2022/01/image-2.png"
      flexDirection="row-reverse"
    />
		<BodyFeature
      titleText="Upload Ribuan Produkmu ke Katalog dalam Hitungan Menit"
      titleDesc="Tanpa ribet, tampilkan seluruh produk kamu dengan berbagai variannya!"
      imageUrl="https://lummoshop.co.id/wp-content/uploads/2022/01/image-3.png"
      flexDirection="row"
    />
		<BodyFeature
      titleText="Fitur Pembayaran & Pengiriman Lengkap"
      titleDesc="Selengkap e-commerce. Memudahkan pembeli-mu memilih jenis pembayaran & pengiriman sesuai kebutuhan."
      imageUrl="https://lummoshop.co.id/wp-content/uploads/2022/01/image-4.png"
      flexDirection="row-reverse"
    />
	</div>
</template>

<script setup>
import BodyFeature from './BodyFeature.vue';

</script>

<style scoped>
.section {
	padding-top: 100px;
	background-color: #eef2ff !important;
	padding-bottom: 40px;
}
.section__container {
	max-width: 775px;
	margin-left: auto;
	margin-right: auto;
	text-align: center;
	font-weight: 500;
	padding-bottom: 20px;
	font-weight: 600;
	animation-delay: 300ms;
	animation-duration: 1200ms;
	animation-name: fadeInUp;
	visibility: visible;
}
.section__title {
	font-size: 2.25rem;
	line-height: 2.5rem;
	color: #1f2937;
}
.section__desc {
	font-size: 16px;
	color: #374151;
	margin-top: var(--spacing-4);
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