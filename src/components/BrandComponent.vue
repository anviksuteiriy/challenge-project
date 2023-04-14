<template>
	<div class="section">
		<BodyFeature
      titleText="Banyak Metode Pembayaran"
      titleDesc="Pembeli bisa memilih metode pembayaran yang paling nyaman untuk mereka. Pilihan mulai dari virtual account/bank transfer, QRIS, e-wallet hingga cash on delivery (COD)."
      imageUrl="https://lummoshop.co.id/wp-content/uploads/2022/01/payment-partners.png"
      flexDirection="row"
    />
		<BodyFeature
      titleText="Berbagai Pilihan Pengiriman"
      titleDesc="Pembelimu juga akan dimudahkan dengan banyaknya jenis pengiriman yang bisa dipilih sesuai yang mereka butuhkan, mulai dari pengiriman reguler, instan dan juga same-day."
      imageUrl="https://www.lummoshop.co.id/wp-content/uploads/2022/02/shipping-partners-20220211.png"
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

@media screen and (max-width: 950px) {
	
}
</style>