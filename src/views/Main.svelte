<script>
    import Languages from './Languages.svelte';
    import { Link } from 'svelte-router'

    import ca from '../../public/texts/ca.md';
	import es from '../../public/texts/es.md';
	import en from '../../public/texts/en.md';

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
	}
	#tools-container{
		margin-left: 45px;
	}
	#tools-container div {
		float: left;
		padding: 5px;
	}
</style>

<Languages changeLang="{changeLang}" />

<div id="text-container">
    {@html text}
</div>

<div id="tools-container">
    <div>Joan</div>
    <div>
        <a href="mailto:joancotros@gmail.com">
            <img width="45" height="30" src="/resources/mail.png"/>
        </a>
    </div>
    <div>
        <a href="#">
            <img width="30" src="/resources/soundcloud.png"/>
        </a>
    </div>
    <div>
        <Link to="/curriculum">CV</Link>
    </div>
</div>
