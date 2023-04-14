<template>
	<div class="section">
		<div class="section__container">
			<div class="section__title">
				Mulai Jualan Online dan Buka Peluang Masa Depan Bisnismu dengan LummoSHOP
			</div>
			<div class="section__desc">
				Miliki toko online dan jual produkmu dengan lebih mudah.
			</div>
			<div style="margin-top: var(--spacing-6);">
				<project-button secondary>Buat Jadwal Demo</project-button>
				<project-button style="margin-left: 10px;">Mulai Sekarang</project-button>
			</div>
		</div>
	</div>
</template>

<script setup>
import ProjectButton from './ProjectButton.vue';
</script>

<style scoped>
.section {
	padding-top: 100px;
	background-color: var(--project-blue);
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
	color: var(--project-green);
}
.section__desc {
	font-size: 16px;
	color: #eae8f4;
	max-width: 615px;
	margin: auto;
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