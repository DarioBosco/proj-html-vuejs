<template>
	<div class="container">
		<div class="text-box">
			<p>Our Products</p>
			<h2>All our delectable pastries are baked fresh in our kitchen every morning, and are made with all-natural, all-organic ingredients</h2>
			<button>Start Shopping</button>
		</div>
		<div class="images-box">
			<div class="arrows">
				<div class="left">
					<i class="fas fa-chevron-left"></i>
				</div>
				<div class="right">
					<i class="fas fa-chevron-right"></i>
				</div>
			</div>
			<div class="image-box">
				<div class="hoverlay">
					<!-- Bellissimo nome per una classe del genere -->
					<h2>Choco Chip Cookies</h2>
					<h6>Cookies, Pastries</h6>
					<h2>$ 19.00 $39.00</h2>
				</div>
				<img src="https://avada.theme-fusion.com/bakery/wp-content/uploads/sites/124/2019/11/choco-chip-cookies.jpg" alt="" />
			</div>
			<div class="image-box">
				<div class="hoverlay">
					<!-- Bellissimo nome per una classe del genere -->
					<h2>Strawberry Jam Cookies</h2>
					<h6>Cookies, Pastries</h6>
					<h2>$ 19.00 $39.00</h2>
				</div>
				<img src="https://avada.theme-fusion.com/bakery/wp-content/uploads/sites/124/2019/11/strawberry-jam-cookies.jpg" alt="" />
			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: 'OurProducts',
};
</script>

<style lang="scss" scoped>
@import '../assets/styles/variables';
@import '../assets/styles/common';
.container {
	display: flex;
	justify-content: center;
	padding-top: 100px;

	.text-box {
		width: calc(100% / 3);
		height: 100px;
		font-family: 'Work Sans';

		& :first-child {
			text-transform: uppercase;
			font-size: 0.75rem;
		}

		& * {
			margin: 20px 0;
		}

		h2 {
			font-family: 'Source Serif Pro';
			color: $daisyBush;
			padding-right: 20%;
			font-size: 2rem;
		}

		button {
			background-color: $daisyBush;
			color: $white;
		}
	}

	.images-box {
		width: calc(100% / 3 * 2);
		height: 720px;
		display: flex;
		align-items: center;
		justify-content: space-between;
		position: relative;

		.arrows {
			position: absolute;
			display: flex;
			justify-content: space-between;
			width: 100%;

			& * {
				background-color: $perfume;
				height: 80px;
				width: 40px;
				display: flex;
				align-items: center;
				justify-content: center;
				color: white;
			}
		}
		.image-box {
			width: calc(50% - 10px);
			height: 100%;
			position: relative;

			.hoverlay {
				position: absolute;
				display: flex;
				flex-direction: column;
				align-items: center;
				justify-content: center;
				visibility: hidden;
				opacity: 0;
				transition: visibility 0s, opacity 0.5s linear;
				color: white;
				background: rgba(53, 49, 49, 0.671);
				height: 100%;
				width: 100%;
			}

			&:hover .hoverlay {
				visibility: visible;
				opacity: 1;
			}

			img {
				width: 100%;
				max-height: 100%;
				object-fit: cover;
			}
		}
	}
}
</style>
