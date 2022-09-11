<script lang="ts">
let index = 0
export default {
	data() {
		return {
			isActive: true,
		}
	},
}
</script>

<template>
	<div class="app-container">
		<header class="title">CSS Animations</header>
		<div class="animation-1" :class="{ active: isActive }">
			<div class="box"></div>
		</div>
		<div class="animation-2" :class="{ active: !isActive }">
			<div id="circle">
				<div id="square"></div>
			</div>
		</div>
		<div class="btn-options">
			<button @click="isActive = !isActive" class="btn-primary">
				toggle animation
			</button>
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
	animation-name: title;
	animation-duration: 2s;
	animation-timing-function: linear;
	animation-delay: 2s;
	animation-iteration-count: infinite;
	animation-direction: normal;
	animation-fill-mode: backwards;
	animation-play-state: running;
}
.animation-1 {
	display: none;
	padding-left: 38%;
	height: 600px;
}
.animation-2 {
	display: none;
	height: 600px;
}
.box {
	width: 100px;
	height: 100px;
	background-color: red;
	position: relative;
	animation: square 4s linear 0s infinite alternate backwards running;
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
	padding: 1rem;
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
		background-color: cornflowerblue;
		left: 0;
		top: 0;
	}
	25% {
		background-color: coral;
		left: 30%;
		top: 0px;
	}
	50% {
		background-color: cornflowerblue;
		left: 30%;
		top: 500px;
		border-radius: 50%;
	}
	70% {
		background-color: aquamarine;
		left: 0px;
		top: 500px;
	}
	100% {
		background-color: darkorange;
		left: 0px;
		top: 0px;
		border-radius: 0px;
	}
}
.active {
	display: flex !important;
}
div#circle {
	width: 200px;
	height: 200px;
	border: 15px solid cornflowerblue;
	margin: 0 auto;
	margin-top: 10%;
	display: flex;
	justify-content: center;
	align-items: center;
	border-radius: 50%;
	animation: circle 2.5s linear 0s infinite forwards;
	/* animation: square 4s linear 0s infinite alternate backwards running; */
}

@keyframes circle {
	0% {
		border-color: darkseagreen;
		transform: scale(1);
	}
	25% {
		border-color: coral;
		transform: scale(1.1);
	}
	50% {
		border-color: cornflowerblue;
		transform: scale(1.3);
	}
	75% {
		border-color: deeppink;
		transform: scale(1.1);
	}
	100% {
		border-color: greenyellow;
		transform: scale(1);
	}
}

div#square {
	width: 75px;
	height: 75px;
	border: 5px solid cornflowerblue;
	animation: square2 2.5s infinite ease-in-out normal;
}

@keyframes square2 {
	0% {
		border-color: darkseagreen;
		transform: rotate(0deg);
	}
	25% {
		border-color: coral;
		border-width: 10px;
	}
	50% {
		border-color: cornflowerblue;
		border-width: 20px;
	}
	75% {
		border-color: deeppink;
		border-width: 40px;
	}
	100% {
		border-color: greenyellow;
		transform: rotate(360deg);
		border-width: 5px;
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
