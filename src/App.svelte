<script lang="ts">
	import Symbol from "./components/Symbol.svelte";
	import Footer from "./components/Footer.svelte";
	import CountryView from "./components/CountryView.svelte";
	import CountryMap from "./components/CountryMap.svelte";

	import strings from "./data/strings";
</script>

<header>
	<Symbol />
	<h1>{strings.title}</h1>
	<p>by Turito Yuenan</p>
</header>

<main>
	<h2>{strings.headings[0]}</h2>
	<ul>
		{#each strings.description as text}
			<li>{text}</li>
		{/each}
	</ul>

	<h2>{strings.headings[1]}</h2>
	<section></section>

	<h2>{strings.headings[2]}</h2>
	<CountryMap />
	<CountryView />
</main>

<Footer />

<style>
	header {
		display: flex;
		flex-direction: column;
		align-items: center;

		text-align: center;
		font-size: 1.5em;

		& h1 {
			margin-top: 0;
			font-size: 2em;
			font-variant: small-caps;
		}
	}

	header p:last-of-type {
		margin-block-end: 0;
	}

	main h2:first-of-type {
		margin-block-start: 0;
	}
</style>
