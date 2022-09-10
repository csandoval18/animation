<script setup lang="ts">
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
</script>

<template>
	<div class="app-container">
		<header class="title">CSS Animations</header>
		<div class="animation-container">
			<div class="box"></div>
		</div>
		<div class="btn-options">
			<button class="btn-primary">next</button>
		</div>
	</div>
</template>

<style scoped>
.app-container {
	display: flex;
	flex-direction: column;
}
.title {
	display: flex;
	align-items: center;
	justify-content: center;
	font-weight: 700;
	height: 8rem;
	font-size: 3rem;
	color: white;
	padding-bottom: 4rem;
}
.animation-container {
	display: flex;
	padding-left: 38%;
	height: 600px;
}
.box {
	width: 100px;
	height: 100px;
	background-color: red;
	position: relative;
	animation: square 4s linear 2s infinite alternate-reverse backwards running;
}
.btn-options {
	margin-top: 3rem;
	display: flex;
	justify-content: center;
	align-items: center;
	background-color: white;
	min-height: 5rem;
}
.btn-primary {
	width: 6rem;
	height: 3rem;
}
/* animation-name: square;
	animation-duration: 2s;
	animation-timing-function: linear;
	animation-delay: 2s;
	animation-iteration-count: infinite;
	animation-direction: normal;
	animation-fill-mode: backwards;
	animation-play-state: running; */
@keyframes square {
	0% {
		background-color: red;
		left: 0;
		top: 0;
	}
	25% {
		background-color: gold;
		left: 30%;
		top: 0px;
	}
	50% {
		background-color: lime;
		left: 30%;
		top: 500px;
		border-radius: 50%;
	}
	70% {
		background-color: dodgerblue;
		left: 0px;
		top: 500px;
	}
	100% {
		background-color: purple;
		left: 0px;
		top: 0px;
		border-radius: 0px;
	}
}
</style>

<!-- 
<script setup lang="ts">
import { ref } from 'vue'

defineProps<{ msg: string }>()

const count = ref(0)
</script>

<template>hello world</template>

<style scoped>
.read-the-docs {
	color: #888;
}
</style> -->
