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
			<nav>
				<ul>
					<li v-for="(link, index) in links.nav" :key="index">
						<a :href="link.link">
							{{ link.name }}<span v-if="link.name == 'Cart'">{{ link.amount }}</span>
						</a>
					</li>
				</ul>
			</nav>
			<div class="footer-bottom">
				<div class="legal">&copy; Copyright 2012 - 2020 | Avada Theme by <a :href="links.legal.themeFusion">ThemeFusion</a>. | All rights reserved. | Powered by <a :href="links.legal.wordpress">Wordpress</a></div>
				<div class="socials"></div>
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
				nav: {
					shop: {
						name: 'Shop',
						link: '#',
					},
					about: {
						name: 'About',
						link: '#',
					},
					gallery: {
						name: 'Gallery',
						link: '#',
					},
					locations: {
						name: 'Locations',
						link: '#',
					},
					journal: {
						name: 'Journal',
						link: '#',
					},
					contacts: {
						name: 'Contacts',
						link: '#',
					},
					order: {
						name: 'Order',
						link: '#',
					},
					cart: {
						name: 'Cart',
						link: '#',
						amount: 0,
					},
				},
				legal: {
					themeFusion: 'https://theme-fusion.com/',
					wordpress: 'https://www.wordpress.com',
				},
				socials: {
					instagram: 'https://www.instagram.com/',
					twitter: 'https://twitter.com/',
					facebook: 'https://facebook.com/',
					pinterest: 'https://pinterest.com/',
				},
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
		justify-content: space-between;
		height: 120px;
		.logo {
			height: 50%;
			img {
				height: 100%;
			}
		}

		h2 {
			color: $primary;
			font-family: 'Source Serif Pro';
			text-align: right;
			padding-bottom: 40px;
		}

		input {
			padding: 8px 10px;
			border: 1px solid $tertiary;
			border-radius: 3px;
			margin-right: 20px;
			width: 400px;
			border: 1px solid lightgrey;
		}

		button {
			background-color: $primary;
			color: $white;
		}
	}
	nav {
		ul {
			list-style: none;

			li {
				display: inline-block;
				margin: 20px;
				font-size: 0.8rem;
				padding-bottom: 5px;

				a {
					text-decoration: none;
					color: $primary;

					span {
						margin-left: 5px;
						display: inline-block;
						background-color: $secondary;
						width: 1.2rem;
						height: 1.2rem;
						line-height: 1.2rem;
						text-align: center;
						border-radius: 50%;
					}
				}
			}
		}
	}
}
</style>
