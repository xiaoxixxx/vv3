<template>
	<div class="peeek-loading center" v-if="loading">
		<div class="cssload-container">
			<div class="cssload-whirlpool"></div>
		</div>
	</div>
</template>

<script setup>
	const loading = ref(false)
	defineExpose({
		loading
	})
</script>

<style lang="scss">
	.peeek-loading {
		background: rgba(0, 0, 0, 0.3);
		bottom: 0;
		left: 0;
		overflow: hidden;
		position: fixed;
		right: 0;
		top: 0;
		z-index: 99999;

	}

	.cssload-container {
		position: relative;
	}

	.cssload-whirlpool,
	.cssload-whirlpool::before,
	.cssload-whirlpool::after {
		position: absolute;
		top: 50%;
		left: 50%;
		border: 1px solid rgb(245,176,76);
		border-left-color: rgb(42,95,100);
		border-radius: 974px;
		-o-border-radius: 974px;
		-ms-border-radius: 974px;
		-webkit-border-radius: 974px;
		-moz-border-radius: 974px;
	}

	.cssload-whirlpool {
		margin: -24px 0 0 -24px;
		height: 49px;
		width: 49px;
		animation: cssload-rotate 1150ms linear infinite;
		-o-animation: cssload-rotate 1150ms linear infinite;
		-ms-animation: cssload-rotate 1150ms linear infinite;
		-webkit-animation: cssload-rotate 1150ms linear infinite;
		-moz-animation: cssload-rotate 1150ms linear infinite;
	}

	.cssload-whirlpool::before {
		content: "";
		margin: -22px 0 0 -22px;
		height: 43px;
		width: 43px;
		animation: cssload-rotate 1150ms linear infinite;
		-o-animation: cssload-rotate 1150ms linear infinite;
		-ms-animation: cssload-rotate 1150ms linear infinite;
		-webkit-animation: cssload-rotate 1150ms linear infinite;
		-moz-animation: cssload-rotate 1150ms linear infinite;
	}

	.cssload-whirlpool::after {
		content: "";
		margin: -28px 0 0 -28px;
		height: 55px;
		width: 55px;
		animation: cssload-rotate 2300ms linear infinite;
		-o-animation: cssload-rotate 2300ms linear infinite;
		-ms-animation: cssload-rotate 2300ms linear infinite;
		-webkit-animation: cssload-rotate 2300ms linear infinite;
		-moz-animation: cssload-rotate 2300ms linear infinite;
	}



	@keyframes cssload-rotate {
		100% {
			transform: rotate(360deg);
		}
	}

	@-o-keyframes cssload-rotate {
		100% {
			-o-transform: rotate(360deg);
		}
	}

	@-ms-keyframes cssload-rotate {
		100% {
			-ms-transform: rotate(360deg);
		}
	}

	@-webkit-keyframes cssload-rotate {
		100% {
			-webkit-transform: rotate(360deg);
		}
	}

	@-moz-keyframes cssload-rotate {
		100% {
			-moz-transform: rotate(360deg);
		}
	}
</style>
