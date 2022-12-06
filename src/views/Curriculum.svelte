<script>
    import Languages from './Languages.svelte';
    import Scroller from '@sveltejs/svelte-scroller';
    import { Link } from 'svelte-router';

    import ca from '../../public/curriculum/ca.md';
	import es from '../../public/curriculum/es.md';
	import en from '../../public/curriculum/en.md';

	let text = ca;

	function changeLang(mouseEvent) {
		const lang = mouseEvent.target.innerText;
		switch(lang) {
			case 'CAST':
				text = es;
				break;
			case 'ENG':
				text = en;
				break;
			default:
				text = ca;
				break;
		}
	}
</script>

<style>
	#text-container {
		max-width: 537px;
		min-width: 400px;
        padding: 5px 0px 10px 50px;
        overflow: scroll;
        text-overflow: ellipsis;
        height: 750px;
        font-size: 11pt;
    }
    .close {
        left: 570px;
        top: 20px;
        position: relative;
        font-size: 20px;
        font-family: sans-serif;
        float:left;
    }
</style>

<Languages changeLang="{changeLang}" />

<div class="close">
    <Link to="/">x</Link>
</div>

<div id="text-container">
     {@html text}
</div>
