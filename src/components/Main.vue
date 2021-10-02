<template>
	<main>
		<OurProducts />
	</main>
</template>

<script>
import OurProducts from './OurProducts.vue';

export default {
	components: {
		OurProducts,
	},
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../assets/styles/variables';
@import '../assets/styles/common';
</style>
