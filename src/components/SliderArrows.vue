<template>
	<div class="silder-arrows-wrap">
		<span class="slider-arrow slider-arrow-left" @click="turn(-1)"> &lt;</span>
		<span class="slider-arrow slider-arrow-right" @click="turn(1)"> &gt;</span>
	</div>
</template>

<script type="es6">
	export default {
		name: 'SliderArrows',
		props: {
			turn: {
				type: Function,
				required: true
			}
		}
	}
</script>

<style>
  span {
    font-size: 14px;
  }
</style>
