<template>
	<header>
		<div class="header-wrapper">
			<div class="header-top">
				<div class="logo">
					<img :src="images.logo" alt="" />
				</div>
				<nav>
					<ul>
						<ul>
							<li v-for="(link, index) in links.nav" :key="index">
								<a v-if="link.name != 'Cart'" :href="link.link">{{ link.name }} </a>
								<a v-else :href="link.link"><i class="fas fa-shopping-cart"></i></a>
							</li>
						</ul>
					</ul>
				</nav>
			</div>
			<div class="jumbotron container">
				<div class="jumbotron-content">
					<p>Fresh & Tasty bakery every day</p>
					<h1>The Perfect Fresh Bread</h1>
					<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Praesentium eius omnis, provident ducimus animi, quisquam velit et mollitia iusto aspernatur unde odio porro architecto, libero dolorem voluptatibus sed suscipit voluptate.</p>

					<button>Explore our products</button>
				</div>
			</div>
		</div>
	</header>
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
					home: {
						name: 'Home',
						link: '#',
					},
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
					contact: {
						name: 'Contact',
						link: '#',
					},
					cart: {
						name: 'Cart',
						link: '#',
						amount: 0,
					},
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

header {
	font-family: 'Work Sans';
	.header-wrapper {
		background-image: url('../assets/img/hero-header-bakery.jpg');
		background-size: cover;
		background-position: top;
		background-repeat: no-repeat;
		.header-top {
			height: 100px;
			display: flex;
			align-items: center;
			justify-content: space-between;
			padding-left: 50px;
			padding-right: 30px;
			nav {
				ul {
					list-style: none;

					li {
						display: inline-block;
						margin: 20px;
						text-transform: uppercase;
						font-size: 0.8rem;
						padding-bottom: 5px;
						border-bottom: 2px solid transparent;

						&:hover {
							border-bottom: 2px solid $primary;
						}

						a {
							text-decoration: none;
							color: $primary;
						}
					}
				}
			}
		}
		.jumbotron-content {
			width: 25%;
			padding-top: 200px;
			padding-bottom: 200px;

			p {
				color: $tertiary;

				&:first-child {
					text-transform: uppercase;
					font-size: 0.75rem;
				}
			}

			h1 {
				color: $primary;
				font-family: 'Source Serif Pro';
				font-size: 3rem;
			}

			& * {
				margin: 20px 0;
			}

			button {
				background-color: $white;
				color: $primary;
			}
		}
	}
}
</style>
