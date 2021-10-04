<template>
	<footer>
		<div class="container">
			<div class="footer-top">
				<div class="logo">
					<img :src="images.logo" alt="" />
				</div>
			</div>
		</div>
	</footer>
</template>

<script>
export default {
	data() {
		return {
			images: {
				logo: 'https://avada.theme-fusion.com/bakery/wp-content/uploads/sites/124/2021/04/avada-bakery-logo.svg',
			},
			links: {
				shop: '#',
				about: '#',
				gallery: '#',
				locations: '#',
				journal: '#',
				contact: '#',
				orders: '#',
				cart: '#',
				allRightsReserved: '',
				wordpress: '#',
				instagram: '#',
				twitter: '#',
				facebook: '#',
				pinterest: '#',
			},
		};
	},
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../assets/styles/variables';
@import '../assets/styles/common';

footer {
	padding-top: 100px;
}
</style>
