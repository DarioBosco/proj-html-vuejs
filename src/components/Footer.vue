<template>
	<footer>
		<div class="container">
			<div class="footer-top">
				<div class="logo">
					<img :src="images.logo" alt="" />
				</div>
				<div class="newsletter">
					<h2>Subscribe to our newsletter</h2>
					<input type="text" name="email" id="email" placeholder="Enter email address" />
					<button>Subscribe</button>
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
				allRightsReserved: '#',
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
	font-family: 'Work Sans';
	padding-top: 100px;
	.footer-top {
		display: flex;
		align-items: center;
		justify-content: space-between;

		h2 {
			color: $primary;
			font-family: 'Source Serif Pro';
		}

		input {
			padding: 6px 10px;
			border: 1px solid $tertiary;
			border-radius: 3px;
		}
	}
}
</style>
