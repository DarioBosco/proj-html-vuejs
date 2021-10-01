<template>
	<header>
		<div class="header-wrapper">
			<div class="logo">
				<img src="https://avada.theme-fusion.com/bakery/wp-content/uploads/sites/124/2021/04/avada-bakery-logo.svg" alt="" />
			</div>
			<nav>
				<ul>
					<li><a href="#">Home</a></li>
					<li><a href="#">Shop</a></li>
					<li><a href="#">About</a></li>
					<li><a href="#">Gallery</a></li>
					<li><a href="#">Locations</a></li>
					<li><a href="#">Journal</a></li>
					<li><a href="#">Contact</a></li>
					<li><a href="#">My Account</a></li>
					<li>
						<a href="#"><i class="fas fa-shopping-cart"></i></a>
					</li>
				</ul>
			</nav>
		</div>
	</header>
</template>

<script></script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../assets/styles/variables';
@import '../assets/styles/common';

header {
	font-family: 'Work Sans';
	.header-wrapper {
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
						border-bottom: 2px solid $daisyBush;
					}

					a {
						text-decoration: none;
						color: $daisyBush;
					}
				}
			}
		}
	}
}
</style>
