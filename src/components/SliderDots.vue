<template>
	<div class="slider-dots-wrap">
		<span class="slider-dot" v-for="i in count" :key="'dot'+ i" :class="{'slider-dot-selected': this.current===i}"
					@click="handleClick(i)">
		</span>
	</div>
</template>

<script type="es6">
	export default {
		name: 'SliderDots',
		props: {
			count: {
				type: Number,
				required: true
			},
			current: {
				type: Number,
				required: true,
				default: 0
			},
			turn: {
				type: Function,
				required: true
			}
		},
		methods: {
			handleClick (i) {
				let option = i - this.current
				this.turn(option)
			}
		}
	}
</script>
