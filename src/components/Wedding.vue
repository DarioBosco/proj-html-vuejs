<template>
	<div id="weddings">
		<div class="container">
			<div class="heading">
				<p>Corporate & Weddings</p>
				<h2>Baking Special Moments</h2>
			</div>
			<div class="images">
				<div id="corp" class="image">
					<div class="hoverlay">
						<!-- Bellissimo nome per una classe del genere -->
						<h6>Interational Bakery</h6>
						<h2>Corporate Events</h2>
						<button>Explore More</button>
					</div>
				</div>
				<div id="wedding" class="image">
					<div class="hoverlay">
						<!-- Bellissimo nome per una classe del genere -->
						<h6>Private Dining Hall</h6>
						<h2>Wedding and Parties</h2>
						<button>Explore More</button>
					</div>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: 'Wedding',
};
</script>

<style lang="scss" scoped>
@import '../assets/styles/variables';
@import '../assets/styles/common';

#weddings {
	margin: 100px 0 0 0;
	.container {
		text-align: center;
		display: flex;
		flex-direction: column;
		justify-content: center;
		.heading {
			p {
				font-family: 'Work Sans';
				text-transform: uppercase;
				color: $tertiary;
				font-size: 0.75rem;
			}

			h2 {
				font-family: 'Source Serif Pro';
				color: $primary;
				font-size: 1.5rem;
			}

			& * {
				margin: 25px 0;
			}
		}
		.images {
			display: flex;
			justify-content: space-between;
			height: 720px;

			.image {
				width: calc(50% - 25px);
				height: 100%;
				background-size: cover;
				position: relative;

				.hoverlay {
					position: absolute;
					display: flex;
					flex-direction: column;
					align-items: center;
					justify-content: center;
					visibility: hidden;
					opacity: 0;
					transition: visibility 0s, opacity 0.3s linear;
					color: white;
					height: 100%;
					width: 100%;
					background-size: cover;
					button {
						background-color: $primary;
						color: $white;
					}

					& * {
						margin: 10px 0;
					}
				}

				&:hover .hoverlay {
					visibility: visible;
					opacity: 1;
				}
			}
			#corp {
				background-image: url('https://avada.theme-fusion.com/bakery/wp-content/uploads/sites/124/2019/11/corporate-bg.jpg');
				& :hover {
					background-image: url('https://avada.theme-fusion.com/bakery/wp-content/uploads/sites/124/2019/11/corporate-hover-bg.jpg');
				}
			}

			#wedding {
				background-image: url('https://avada.theme-fusion.com/bakery/wp-content/uploads/sites/124/2019/11/wedding-bg.jpg');
				& :hover {
					background-image: url('https://avada.theme-fusion.com/bakery/wp-content/uploads/sites/124/2019/11/wedding-hover-bg.jpg');
				}
			}
		}
	}
}
</style>
