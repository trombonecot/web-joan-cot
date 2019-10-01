<script>
    export let changeLang;
</script>

<style>
	#languages {
		float: right;
		margin-right: 30px;
    	margin-top: 10px;
	}
	#languages span{
		color: white;
		padding-right: 20px;
        cursor: pointer;
	}
</style>

<div id="languages">
    <span  on:click={changeLang}>CAT</span>
    <span  on:click={changeLang}>CAST</span>
    <span  on:click={changeLang}>ENG</span>
</div>