<script lang="ts">
	import "../app.css";
	import { page } from '$app/state';
	import favicon from '$lib/assets/favicon.svg';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

<nav>
	<a href="/">home</a>
	<a href="/blog">blog</a>
	<a href="/message">message</a>
	<a href="/about">about</a>
</nav>

<h1>---</h1>

<p>
	URL = {page.url}
</p>
<p>
	PARAMS = {JSON.stringify(page.params)}
</p>
<p>
	ROUTE = {JSON.stringify(page.route)}
</p>
<p>
	STATE = {JSON.stringify(page.state)}
</p>
<p>
	DATA = {JSON.stringify(page.data)}
</p>
<p>
	STATUS = {JSON.stringify(page.status)}
</p>
<p>
	ERROR = {JSON.stringify(page.error)}
</p>


{@render children()}
