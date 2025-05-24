<script>
    import { page } from "$app/state";
    import YouTubeVideo from "components/YouTubeVideo.svelte";

    const STARS = [
        "PotVC First Star",
        "PotVC Replica"
    ];

    let star = $derived(Number(page.params.star));
    let route = $derived.by(() => {
        const split = page.url.pathname.split('/');
        return split[split.length - 1];
    });
</script>

<h1>RTA Guide/Puzzle of the Vanish Cap</h1>

<p>
    Puzzle of the Vanish Cap is one of the 3 cap stages (the Vanish Cap one). It is located in a hiden pipe inside Gloomy Garden. 8 Stars are required to enter it as entering Gloomy Garden requires 8 Stars.
</p>

<h2>Stars</h2>

<ol>
    {#each STARS as s, i}
        <li class:active={star === i + 1}><a href="{isNaN(star) ? `${route}/` : ''}{i + 1}">{s}</a></li>
    {/each}
</ol>

<h2>{STARS[star - 1]}</h2>

{#if star === 1}
    <h3>Beginner</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/mQ6gnW2JziU?si=t6Hj6yj31hRmi6XJ"></YouTubeVideo>

    <h3>Intermediate</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/kGC9LTLt9PE?si=eQiY3TQAtdjn2uZ_"></YouTubeVideo>

    <h2>Movements (Grave to Pipe)</h2>
    <YouTubeVideo src="https://www.youtube.com/embed/Mpih9NXhULA?si=yR7ckSKgJDwRioAg"></YouTubeVideo>

    <h2>Strats</h2>

    <h3>Beginner</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/pjq2xxOXjJI?si=gJ8u7ZafUcaiNlaR"></YouTubeVideo>

    <h3>Advanced</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/GS_qWkJVnTA?si=x0LombpOGhRiczHx"></YouTubeVideo>
{:else if star === 2}
    <h3>Beginner</h3>
{/if}
