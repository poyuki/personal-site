<script>
	import { page } from '$app/stores';

	export let path;
	export let title;
</script>

<a
	class:active={$page.url.pathname === path}
	class="nav-link"
	href="{path}">
	{title}
</a>