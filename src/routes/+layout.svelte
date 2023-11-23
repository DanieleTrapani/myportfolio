<script lang="ts">
	import '../app.pcss';
	import { page } from '$app/stores';
	const pathname = $page.url.pathname;

	const changeActive = (event: any) => {
		if (event.target.classList.contains('active')) {
			return;
		} else {
			const active = document.querySelector('.active');
			active?.classList.remove('active');
			active?.classList.add('inactive');
			event.target.classList.add('active');
		}
	};
</script>

<header class="flex justify-center p-4">
	<div class="flex gap-1 bg-gray-300 px-3 py-1 rounded-full">
		<a
			href="/"
			class="header-link {pathname === '/' ? 'active' : 'inactive'}"
			on:click={() => changeActive(event)}>About</a
		>
		<a
			href="/projects"
			class="header-link {pathname === '/projects' ? 'active' : 'inactive'}"
			on:click={() => changeActive(event)}>Projects</a
		>
		<a
			href="/contact"
			class="header-link {pathname === '/contact' ? 'active' : 'inactive'}"
			on:click={() => changeActive(event)}>Contact</a
		>
	</div>
</header>
<slot />

<style lang="postcss">
	.header-link {
		@apply rounded-full px-3 py-1 text-xs;
	}
	.active {
		@apply bg-gray-50 font-bold shadow-md;
	}

	.inactive {
		@apply duration-300 hover:bg-gray-100;
	}
</style>
