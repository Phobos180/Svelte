<script>
	import { page } from '$app/stores';
</script>

{#if $page.url.pathname.startsWith('/users')}
	<slot />
{:else}
	<div style:background="yellow">
		<nav>
			<a href="/">Home</a>
			<a href="/about">About</a>
		</nav>

		<slot />

		<footer style:margin-top="60px">All rights reserved</footer>
	</div>
{/if}
