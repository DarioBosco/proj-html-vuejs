<template>
	<main> 
		<OurProducts />
		<Wedding />
	</main>
</template>

<script>
import OurProducts from './OurProducts.vue';
import Wedding from './Wedding.vue';

export default {
	components: {
		OurProducts,
		Wedding,
	},
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../assets/styles/variables';
@import '../assets/styles/common';
</style>
