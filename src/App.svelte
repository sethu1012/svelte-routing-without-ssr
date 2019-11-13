<script>
	import { Router, Link, Route } from 'svelte-routing';
	import Page1 from '../pages/Page1.svelte';
	import Page2 from '../pages/Page2.svelte';
	export let url = "/";
</script>

<Router url="{url}">
	<nav>
		<Link to="page1">Page 1</Link>
		<Link to="page2">Page 2</Link>
  	</nav>
	<div>
		<Route path="page1" component={Page1} />
		<Route path="page2" component={Page2} />
		<Route path="/">
			<Page1 />
		</Route>
	</div>
</Router>