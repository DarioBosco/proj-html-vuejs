<template>
	<div class="container">
		<div class="text-box">
			<p>Our Products</p>
			<h2>All our delectable pastries are baked fresh in our kitchen every morning, and are made with all-natural, all-organic ingredients</h2>
			<button>Start Shopping</button>
		</div>
		<div class="images-box">
			<div class="image-box">
				Immagine
			</div>
			<div class="image-box">
				Immagine
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
	align-items: center;
	justify-content: center;

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
		}

		button {
			background-color: $daisyBush;
			color: $white;
		}
	}

	.images-box {
		width: calc(100% / 3 * 2);
		height: 100px;
		display: flex;
		align-items: center;
		justify-content: space-between;
		.image-box {
			background: red;
			width: calc(50% - 10px);
		}
	}
}
</style>
