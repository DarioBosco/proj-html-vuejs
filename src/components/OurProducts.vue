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
.container {
	display: flex;
	align-items: center;
	justify-content: center;

	.text-box {
		width: calc(100% / 3);
		height: 100px;
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
