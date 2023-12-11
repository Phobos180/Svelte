<script>
	import { page } from '$app/stores';

	$: console.log($page);
</script>

<h1>Users Page</h1>

<p>Users ID: {$page.params.id}</p>
