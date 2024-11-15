<script>
	import ListItem from '$lib/fonts/components/ListItem.svelte';
	export let data;
</script>

<h1 style="font-size: 25px; margin-top: 2rem;">
	Welcome to the <strong class="text-primary">Fronted Quiz</strong>
</h1>
<p>Pick a subject to get started</p>
<br />

<div class="flex flex-col gap-4">
	{#each data.quizzes as quiz, index (quiz.title)}
		<a href="/{quiz.title.toLowerCase()}"><ListItem title={quiz.title} {index} /></a>
	{/each}
</div>
