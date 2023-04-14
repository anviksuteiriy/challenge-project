<template>
	<div class="section">
		<div class="section__container">
			<div class="section__title">
				Ada Pertanyaan? Temukan Jawabannya di Sini!
			</div>
		</div>
		<div class="accordian__container">
			<div v-for="c of contents" :key="c.title" class="card__container">
			<div class="title" @click="c.expanded = !c.expanded">
				<div>
					<b>{{ c.title }}</b>
				</div>
				<div>
					<i v-if="c.expanded" class="fa fa-angle-right"></i>
          <i v-else class="fa fa-angle-down"></i>
				</div>
			</div>
			<div class="description" v-if="c.expanded">
				<div v-html="c.description"></div>
			</div>
		</div>
		</div>
	</div>
</template>

<script setup>
import { ref } from 'vue';
const contents = ref(
	[
		{
			title: "Apa kelebihan utama membuat website toko online pakai LummoSHOP?",
      description: "<p>Pertama, jadi mudah kelola produk di katalog online. Bisa atur produk, foto, deskripsi, dan info ketersediaan produk langsung dari satu dashboard.</p><p>Kedua, lebih mudah jangkau pelanggan secara online semudah share status dan link kepada calon pembeli potensial lewat Whatsapp atau akun media sosial. Bisa share link toko online-mu atau link produk spesifik yang ada di katalogmu.</p><p>Ketiga, tersedia berbagai pilihan pembayaran untuk pelanggan dengan fitur link pembayaran LummoSHOP yang 100% aman terverifikasi Bank Indonesia dan bebas biaya transfer antar bank. Bisa transfer dari bank manapun atau e-wallet.</p><p>Keempat, bisa atur pesanan dan pengiriman produk dari satu aplikasi. Pesanan dan pengiriman bisa dipantau dan dilakukan langsung dalam satu dashboard.</p><p></p>",
      expanded: false,
		},
		{
			title: "Apakah akan ada fitur-fitur baru?",
      description: "<p>Kami akan segera memperbarui LummoSHOP dengan lebih banyak fitur yang membantu kamu jualan online lebih maksimal, seperti bulk upload produk, pilihan kurir pengiriman yang lebih banyak, dan lainnya.</p>",
      expanded: false,
		},
		{
			title: "Apakah aplikasi ini gratis?",
      description: "<p>LummoSHOP akan selalu GRATIS untuk diunduh dan membantu kamu dalam membuat website toko online pribadi langsung dari HP secara mudah. Hanya ada potongan biaya layanan transaksi sebesar 2,5% (untuk kategori makanan dan minuman) dan 1% (untuk kategori lainnya) dari total pembayaran di luar biaya pengiriman. Fitur LummoSHOP lainnya GRATIS digunakan tanpa dikenakan biaya dan kamu juga bebas unggah produk sebanyak-banyaknya.</p>",
      expanded: false,
		},
		{
			title: "Apa kelebihan utama membuat website toko online pakai LummoSHOP?",
      description: "<p>Pertama, jadi mudah kelola produk di katalog online. Bisa atur produk, foto, deskripsi, dan info ketersediaan produk langsung dari satu dashboard.</p><p>Kedua, lebih mudah jangkau pelanggan secara online semudah share status dan link kepada calon pembeli potensial lewat Whatsapp atau akun media sosial. Bisa share link toko online-mu atau link produk spesifik yang ada di katalogmu.</p><p>Ketiga, tersedia berbagai pilihan pembayaran untuk pelanggan dengan fitur link pembayaran LummoSHOP yang 100% aman terverifikasi Bank Indonesia dan bebas biaya transfer antar bank. Bisa transfer dari bank manapun atau e-wallet.</p><p>Keempat, bisa atur pesanan dan pengiriman produk dari satu aplikasi. Pesanan dan pengiriman bisa dipantau dan dilakukan langsung dalam satu dashboard.</p><p></p>",
      expanded: false,
		},
		{
			title: "Apakah akan ada fitur-fitur baru?",
      description: "<p>Kami akan segera memperbarui LummoSHOP dengan lebih banyak fitur yang membantu kamu jualan online lebih maksimal, seperti bulk upload produk, pilihan kurir pengiriman yang lebih banyak, dan lainnya.</p>",
      expanded: false,
		},
		{
			title: "Apakah aplikasi ini gratis?",
      description: "<p>LummoSHOP akan selalu GRATIS untuk diunduh dan membantu kamu dalam membuat website toko online pribadi langsung dari HP secara mudah. Hanya ada potongan biaya layanan transaksi sebesar 2,5% (untuk kategori makanan dan minuman) dan 1% (untuk kategori lainnya) dari total pembayaran di luar biaya pengiriman. Fitur LummoSHOP lainnya GRATIS digunakan tanpa dikenakan biaya dan kamu juga bebas unggah produk sebanyak-banyaknya.</p>",
      expanded: false,
		},
	]
);
</script>

<style scoped>
.section {
	padding-top: 40px;
	background-color: #ffffff !important;
	padding-bottom: 40px;
}
.section__container {
	max-width: 800px;
	margin-left: auto;
	margin-right: auto;
	text-align: center;
	padding-bottom: 20px;
	font-weight: 600;
}
.section__title {
	font-size: 2rem;
	line-height: 2.5rem;
	color: #1f2937;
	margin-bottom: 40px;
}
.accordian__container {
	display: flex;
	flex-wrap: wrap;
	justify-content: space-around;
	align-items: baseline;
}
.card__container {
	background: #eae8f4;
	border: 1px solid #ada4d3;
	border-radius: 4px;
	padding-left: 25px;
	padding-right: 25px;
	margin-bottom: 25px;
	width: 40%;
	font-size: 14px;
	text-align: left;
}
.card__container--expanded {
	height: auto;
}
.title {
  cursor: pointer;
  display: flex;
  justify-content: space-between;
}
.title,
.description {
  padding: 12px;
}
@media screen and (max-width: 950px) {
	.section__title {
		font-size: 1.5rem;
		line-height: 2.125rem;
	}
	.section__container {
		padding: var(--spacing-4);
	}

	.card__container {
		width: 80%;
	}
}
</style>