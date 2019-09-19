<script>
	import ca from '../public/texts/ca.md';
	import es from '../public/texts/es.md';
	import en from '../public/texts/en.md';

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
	#main {
		font-family: 'Saira Extra Condensed', sans-serif;
		font-size: 13pt;
		background-image: url('/resources/bg.png');
		background-size: 100%;
		background-repeat: no-repeat;
		height: 1024px;
		width: 1600px;
		margin: 0 auto;
	}
	#text-container {
		max-width: 537px;
		min-width: 400px;
		padding: 5px 0px 10px 50px;
	}
	#languages {
		float: right;
		margin-right: 30px;
    	margin-top: 10px;
	}
	#languages a{
		color: white;
		padding-right: 20px;
	}
	#tools-container{
		margin-left: 45px;
	}
	#tools-container div {
		float: left;
		padding: 5px;
	}
</style>

<div id="main">
	<div id="languages">
		<a href="#"  on:click={changeLang}>CAT</a>
		<a href="#"  on:click={changeLang}>CAST</a>
		<a href="#"  on:click={changeLang}>ENG</a>
	</div>

	<div id="text-container">
		{@html text}
	</div>

	<div id="tools-container">
		<div>Joan</div>
		<div>
			<a href="mailto:joancotros@gmail.com">
				<img width="30" height="20" src="/resources/mail.png"/>
			</a>
		</div>
		<div>
			<a href="#">
				<img width="30" height="20" src="/resources/soundcloud.png"/>
			</a>
		</div>
		<div>
			<a href="#">
				pdf
			</a>
		</div>
	</div>
</div>
