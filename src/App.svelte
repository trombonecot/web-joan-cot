<script>
  	import SvelteRouter, { Link } from 'svelte-router';

	import Main from './views/Main.svelte';
	import Curriculum from './views/Curriculum.svelte';
	
	function create (node) {
		const router = new SvelteRouter({
		target: node,
		mode: 'hash',
		routes: [{
				path: '/',
				component: Main
			}, {
				path: '/curriculum',
				component: Curriculum
			}]
		});
	
		return {
			destroy () {
				router.destroy()
			}
		};
	}
</script>

<style>
	#main {
		font-family: 'Saira Semi Condensed', sans-serif;
		font-size: 12pt;
		background-image: url('/resources/bg.jpg');
		background-size: 100%;
		background-repeat: no-repeat;
		height: 855px;
		width: 1366px;
		margin: 0 auto;
		margin-top: 25px;
	}
</style>

<div id="main">
	<div use:create></div>
</div>
