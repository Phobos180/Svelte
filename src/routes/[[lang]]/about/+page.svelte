<script>
	import { goto, beforeNavigate, afterNavigate } from '$app/navigation';
	import { Button } from '$components';
	import { navigating, page } from '$app/stores';

	$: console.log(navigating);

	{
		JSON.stringify($page.params);
	}
</script>

<h1>Welcome to About</h1>
