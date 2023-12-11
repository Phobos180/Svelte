<script lang="ts">
	import { goto, beforeNavigate, afterNavigate } from '$app/navigation';
	import { Button } from '$components';
	import { navigating, page } from '$app/stores';

	$: console.log(navigating);

	let currentPage = 'en/about';
	let text = 'Ciaone';

	beforeNavigate((navigation) => {
		console.log('beforeNavigate', navigation);
	});

	afterNavigate((navigation) => {
		console.log('afternavigate', navigation);
	});

	const handleButtonClick = () => {
		// Do something when the button is clicked
		// This function is invoked when the button inside Button.svelte is clicked
		console.log('Button clicked from Homepage');
	};
</script>

<h1>Welcome to SvelteKit</h1>
<Button {text} {currentPage} />
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>
