<script>
	import SiteHeader from '$lib/SiteHeader.svelte';
	import SiteFooter from '$lib/SiteFooter.svelte';
	import { SUBMIT_URL } from '$lib/links.js';
</script>

<svelte:head>
	<title>Ghost Ship | Requirements</title>
</svelte:head>

<div class="page">

<SiteHeader current="requirements" />

<main>
	<header class="intro">
		<p class="eyebrow">Ship it, get candy</p>
		<h1>Requirements</h1>
		<p>Everything your game needs before it counts. A small finished game beats a big unfinished one: only shipped games get candy.</p>
	</header>

	<section class="block">
		<h2><i class="ph-bold ph-check-circle"></i>Your game must</h2>
		<ul>
			<li><strong>Start from the p5.js starter.</strong> Don't begin from a blank sketch: the core loop (spawn → click → score) must already run.</li>
			<li><strong>Be playable end to end.</strong> A start screen, a play state, and a game-over screen, even if bare-bones.</li>
			<li><strong>Be ghost or Halloween-themed.</strong> Ghosts, pumpkins, bats, haunted houses: anything spooky.</li>
			<li><strong>Add 1-3 upgrades of your own.</strong> Movement, sound, lives, power-ups, a boss. Not ten, just a few that work.</li>
			<li><strong>Credit your assets.</strong> Self-made, or linked from a free-use source in your README.</li>
		</ul>
	</section>

	<section class="block">
		<h2><i class="ph-bold ph-scales"></i>Fair play</h2>
		<ul>
			<li>Talk with your neighbor, but don't paste their file. Two people submitting the same code both need to have built it.</li>
			<li>AI is fine for unblocking a single line, not for writing your upgrade.</li>
			<li>Sound and art from OpenGameArt, Kenney.nl, or Freesound: link the source.</li>
		</ul>
	</section>

	<section class="block">
		<h2><i class="ph-bold ph-upload-simple"></i>What to submit</h2>
		<ul>
			<li><strong>Playable link:</strong> the p5.js Web Editor share link, or a GitHub Pages URL.</li>
			<li><strong>Source:</strong> the editor link already has it, or attach a repo.</li>
			<li><strong>One GIF or ~20-second clip</strong> of the game being played.</li>
			<li><strong>Two sentences:</strong> which upgrades you added, and why.</li>
			<li><strong>Your name / Slack handle,</strong> so we know who to hand candy to.</li>
		</ul>
	</section>

	<section class="block faq">
		<h2><i class="ph-bold ph-question"></i>Quick answers</h2>
		<dl>
			<dt>What if I don't finish?</dt>
			<dd>Ship what you've got. A working base game with zero upgrades still counts: the bar is a playable link, not a polished product.</dd>
			<dt>Do I need to install anything?</dt>
			<dd>No. Everything runs in the p5.js Web Editor in a browser tab.</dd>
			<dt>Is there a deadline?</dt>
			<dd>The end of the meeting. Submissions and candy happen live at the showcase.</dd>
		</dl>
	</section>

	<div class="cta">
		<a class="btn primary" href="/tutorial/"><i class="ph-bold ph-book-open"></i>Start the guide</a>
		<a class="btn ghost" href={SUBMIT_URL}><i class="ph-bold ph-rocket-launch"></i>Submit your game</a>
	</div>
</main>

<SiteFooter />
</div>

<style>
	:global(:root) {
		--night: #14101c;
		--panel: #1d1728;
		--panel-line: #372c46;
		--parchment: #f4ecd9;
		--parchment-dim: #b8ab99;
		--pumpkin: #ff8f3f;
		--mint: #8fd6b0;
		--font-display: 'Griffy', cursive;
		--font-body: 'Phantom Sans', system-ui, -apple-system, 'Segoe UI', sans-serif;
	}
	:global(*) {
		box-sizing: border-box;
	}
	.page {
		min-height: 100vh;
		min-height: 100dvh;
		display: flex;
		flex-direction: column;
		background: var(--night);
		color: var(--parchment);
		font-family: var(--font-body);
	}
	main {
		flex: 1;
		width: 100%;
		max-width: 820px;
		margin: 0 auto;
		padding: clamp(24px, 5vh, 56px) 20px 56px;
	}
	.intro {
		margin-bottom: 28px;
	}
	.eyebrow {
		margin: 0 0 8px;
		color: var(--mint);
		font-size: 13px;
		font-weight: 700;
		text-transform: uppercase;
		letter-spacing: 0.06em;
	}
	h1 {
		font-family: var(--font-display);
		font-size: clamp(2.6rem, 6vw, 3.8rem);
		line-height: 1.05;
		margin: 0 0 12px;
	}
	.intro p:last-child {
		color: var(--parchment-dim);
		font-size: 1.1rem;
		line-height: 1.6;
		margin: 0;
		max-width: 60ch;
	}
	.block {
		background: var(--panel);
		border: 1px solid var(--panel-line);
		border-radius: 12px;
		padding: 22px 26px;
		margin-bottom: 16px;
	}
	.block h2 {
		display: flex;
		align-items: center;
		gap: 10px;
		font-family: var(--font-display);
		font-size: 1.45rem;
		margin: 0 0 12px;
	}
	.block h2 i {
		color: var(--pumpkin);
	}
	ul {
		margin: 0;
		padding-left: 20px;
		display: grid;
		gap: 8px;
		color: var(--parchment-dim);
		line-height: 1.6;
	}
	strong {
		color: var(--parchment);
	}
	dl {
		margin: 0;
	}
	dt {
		font-weight: 700;
		margin-top: 12px;
	}
	dt:first-child {
		margin-top: 0;
	}
	dd {
		margin: 4px 0 0;
		color: var(--parchment-dim);
		line-height: 1.6;
	}
	.cta {
		display: flex;
		gap: 12px;
		flex-wrap: wrap;
		margin-top: 24px;
	}
	.btn {
		display: inline-flex;
		align-items: center;
		gap: 8px;
		font-size: 15px;
		font-weight: 700;
		text-decoration: none;
		padding: 12px 22px;
		border-radius: 999px;
		border: 2px solid var(--panel-line);
		color: var(--parchment);
	}
	.btn.primary {
		background: var(--pumpkin);
		border-color: var(--pumpkin);
		color: #241505;
	}
	.btn.ghost:hover {
		border-color: var(--pumpkin);
		color: var(--pumpkin);
	}
</style>
