<script lang="ts">
	import { goto } from '$app/navigation';

	export let currentPage: string;
	export let text: string;

	// Function to handle click and trigger navigation
	const handleClick = () => {
		if (currentPage) {
			goto(currentPage);
		}
	};
</script>

<button on:click={handleClick}>{text} {currentPage}</button>
