<script>
	import Go from '$lib/icons/go.svg';
	import Python from '$lib/icons/python.svg';
	import Rails from '$lib/icons/rails.svg';
	import React from '$lib/icons/react.svg';
	import Rust from '$lib/icons/rust.svg';
	import Svelte from '$lib/icons/svelte.svg';
	import Tailwind from '$lib/icons/tailwind.svg';
	import TypeScript from '$lib/icons/typescript.svg';

	const iconWidth = 50;
</script>

<main class="px-16">
	<div class="bg-white p-4 rounded-2xl flex flex-col gap-3 mb-5">
		<h4>Hi! My name is <br /><span class="font-bold text-4xl">Daniele.</span></h4>
		<p>I'm a Software Developer based in the Netherlands 🇳🇱</p>
		<p>
			I'm a nerd with a deep love for programming, find below some of my favourite tools and
			languages in my development stack
		</p>
	</div>

	<div class="bg-white p-4 rounded-2xl">
		<h4 class="font-bold text-xl mb-2">Tech Stack</h4>
		<div class="flex gap-3 flex-wrap justify-between svg-container">
			<a href="https://www.typescriptlang.org" target="_blank">
				<img src={TypeScript} alt="TypeScript" class="tech-svg" />
			</a>
			<a href="https://rubyonrails.org/" target="_blank">
				<img src={Rails} alt="Rails" class="tech-svg" />
			</a>
			<a href="https://reactjs.org/" target="_blank">
				<img src={React} alt="React" class="tech-svg" />
			</a>
			<a href="https://svelte.dev/" target="_blank">
				<img src={Svelte} alt="Svelte" class="tech-svg" />
			</a>
			<a href="https://tailwindcss.com/" target="_blank">
				<img src={Tailwind} alt="Tailwind" class="tech-svg" />
			</a>
			<a href="https://www.python.org/" target="_blank">
				<img src={Python} alt="Python" class="tech-svg" />
			</a>
			<a href="https://golang.org/" target="_blank">
				<img src={Go} alt="Golang" class="tech-svg" />
			</a>
			<a href="https://www.rust-lang.org/" target="_blank">
				<img src={Rust} alt="Rust" class="tech-svg" />
			</a>
		</div>
	</div>
</main>

<style lang="postcss">
	span {
		background: -webkit-linear-gradient(left, #037bcb, #00a870);
		-webkit-background-clip: text;
		-webkit-text-fill-color: transparent;
	}

	@media (min-width: 375px) {
		.tech-svg {
			width: 50px;
		}
	}

	@media (min-width: 768px) {
		.tech-svg {
			width: 65px;
		}

		.svg-container {
		}
	}

	@media (min-width: 1024px) {
		main {
			@apply px-48;
		}
	}
</style>
