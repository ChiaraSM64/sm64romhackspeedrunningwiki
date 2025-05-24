<script>
    import { page } from "$app/state";
    import YouTubeVideo from "components/YouTubeVideo.svelte";

    const STARS = [
        null,
        "BRR Replica",
        "Boss Entry",
        "Boss Fight"
    ];

    let star = $derived(Number(page.params.star));
    let route = $derived.by(() => {
        const split = page.url.pathname.split('/');
        return split[split.length - 1];
    });
</script>

<h1>RTA Guide/Bowser's Rainbow Rumble</h1>

<p>
    Bowser's Rainbow Rumble is the last Bowser Course of Super Mario Star Road. It is located above the clouds, on the star road, behind the 80 Star door.
    Key 1, Key 2, and 80 Stars are required to enter this level without the BLJ strat.
</p>

<h2>Stars</h2>

<ol>
    {#each STARS as s, i}
        {#if s}
            <li class:active={star === i + 1}><a href="{isNaN(star) ? `${route}/` : ''}{i + 1}">{s}</a></li>
        {/if}
    {/each}
</ol>

<h2>{STARS[star - 1]}</h2>

{#if star === 1}
    <h3>Beginner</h3>
{:else if star === 2}
    <h3>Beginner</h3>
{:else if star === 3}
    <h3>Beginner</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/aojfycX59dw?si=lNGMarfH4wlt9hev"></YouTubeVideo>

    <h3>Intermediate</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/pm_BPAiDDOM?si=bjE6779rzcYGx8ug"></YouTubeVideo>

    <h3>Advanced</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/mZUqzWMYfqA?si=kweg2CB6d63H331M"></YouTubeVideo>
{:else if star === 4}
    <YouTubeVideo src="https://www.youtube.com/embed/2Zu8-CkBzPc?si=nN3wJSqRmEqOa9Cs"></YouTubeVideo>
{/if}
