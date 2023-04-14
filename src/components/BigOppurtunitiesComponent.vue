<template>
	<div class="section">
		<div class="section__container">
			<div class="section__title">
				Langkah Kecil untuk Membuka Peluang Besar
			</div>
			<div class="section__desc">
				Ikuti 4 langkah di bawah ini untuk mempercepat bisnis online-mu!
			</div>
		</div>
		<div class="row__container">
			<BodyFeature2
				captionText="LANGKAH 1"
				titleText="Mulai Bikin Toko Online-mu"
				titleDesc="Masukkan nama brand-mu dan pastikan sesuai dengan nama yang tertera pada link website untuk mempermudah branding toko online-mu."
				imageUrl="https://lummoshop.co.id/wp-content/uploads/2022/01/image-step-1.png"
				flexDirection="column-reverse"
			/>
			<BodyFeature2
				captionText="LANGKAH 2"
				titleText="Verifikasi Akun"
				titleDesc="Untuk meningkatkan kepercayaan pembeli belanja di tokomu, lakukan verifikasi akun toko online-mu sedini mungkin."
				imageUrl="https://lummoshop.co.id/wp-content/uploads/2022/01/image-step-2.png"
				flexDirection="column-reverse"
			/>
		</div>
		<div class="row__container">
			<BodyFeature2
				captionText="LANGKAH 3"
				titleText="Buat Katalog"
				titleDesc="Tampilkan foto-foto terbaik seluruh produk jualanmu atau jasamu, berikan deskripsi yang lengkap, dan lengkapi pilihan metode pembayaran serta pengiriman."
				imageUrl="https://lummoshop.co.id/wp-content/uploads/2022/01/image-step-3.png"
				flexDirection="column-reverse"
			/>
			<BodyFeature2
				captionText="LANGKAH 4"
				titleText="Maksimalkan Penjualanmu!"
				titleDesc="Gunakan fitur-fitur pemasaran dan analisa data pelanggan kami, agar promosi kamu bisa sampai di calon-calon pembeli yang tepat!"
				imageUrl="https://lummoshop.co.id/wp-content/uploads/2022/01/image-step-4.png"
				flexDirection="column-reverse"
			/>
		</div>
	</div>
</template>

<script setup>
import BodyFeature2 from './BodyFeature2.vue';

</script>

<style scoped>
.section {
	padding-top: 100px;
	background-color: #ffffff !important;
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

.row__container {
	display: flex;
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

	.row__container {
		flex-direction: column;
	}
}
</style>