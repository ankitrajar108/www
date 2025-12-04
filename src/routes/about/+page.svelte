<script>
	import GithubIcon from '~icons/ph/github-logo';
	import DiscordIcon from '~icons/ph/discord-logo';
	import KofiIcon from '~icons/ph/coffee';
	import XIcon from '~icons/ph/x-logo';

	let content = {
		tech: {
			languages: ['js', 'ts', 'python', 'php', 'html', 'css'],
			frameworks: ['node.js', 'express', 'react', 'next.js'],
			databases: ['mysql', 'mongodb'],
			tools: ['vscode', 'git']
		}
	};
</script>

<main>
	<h1>about</h1>
	<p>
		hey there! i'm ankit yadav, a self-taught web developer who loves building practical tools and clean web experiences. i enjoy experimenting with new ideas, learning fast, and creating projects that help real users. i love making things that are both functional and beautiful.
	</p>
	<h2>links</h2>
	<div class="links">
		<a href="https://github.com/ankitrajar108" class="external icon">
			<GithubIcon /><span class="text">github</span><span class="arrow">/></span>
		</a>
		<a href="https://x.com/ruvtyy" class="external icon">
			<XIcon /><span class="text">x/twitter</span><span class="arrow">/></span>
		</a>
	</div>
	<!-- <h2>languages</h2>
	{#each Object.keys(content.languages) as category}
		<div class="info">
			{category} <span class="sub">-></span>
			{#each content.languages[category] as item}
				{item}
				{#if item !== content.languages[category][content.languages[category].length - 1]}
					<span class="sub">/</span>&nbsp;
				{/if}
			{/each}
		</div>
	{/each} -->
	<h2>tech</h2>
	{#each Object.keys(content.tech) as category}
		<div class="info">
			{category} <span class="sub">-></span>
			{#each content.tech[category] as item}
				{item}
				{#if item !== content.tech[category][content.tech[category].length - 1]}
					<span class="sub">/</span>&nbsp;
				{/if}
			{/each}
		</div>
	{/each}
</main>

<style>
	main {
		width: 100%;
		max-width: 53rem;
		margin: 0 auto 10rem auto;
		padding: 0 1.5rem;
	}

	a {
		font-family: 'Space Mono', monospace;
		font-size: 1.25rem;
		margin: 0.5rem 0;
		display: block;
	}

	.info {
		font-size: 1.125rem;
		margin: 0.5rem 0;
		font-family: 'Space Mono', monospace;
	}

	.webring {
		display: inline-block;
		margin: 0;
		span {
			display: inline-block;
			transition: 0.2s;
		}
		&.home:hover {
			text-decoration: underline 2px;
		}
		&.next:hover span {
			transform: translateX(0.3em);
		}
		&.previous:hover span {
			transform: translateX(-0.3em);
		}
	}

	.card {
		margin: 0;
		display: inline;
		width: 88px;
		height: 31px;

		img {
			image-rendering: pixelated;
			width: 88px;
			height: 31px;
		}
	}

	.colors {
		display: inline-flex;
		margin-top: 0.5rem;
		flex-wrap: wrap;
	}

	.color {
		display: inline-block;
		padding: 0 0.5rem;
		width: 5rem;
		text-align: center;
		font-size: 1.125rem;
	}
</style>
