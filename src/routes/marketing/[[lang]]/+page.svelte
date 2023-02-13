<script lang="ts">
	import { page } from '$app/stores';
	const greetings = {
		en: 'Hello!',
		es: 'Hola!',
		fr: 'Bonjour!'
	};
	const { lang = 'en' } = $page.params;
	const greeting = greetings[lang as keyof typeof greetings]; // typescript
</script>

{#if greeting}
	<h1>{greeting}</h1>
{:else}
	<h1>NO Greeting for lang [{lang}]</h1>
{/if}
