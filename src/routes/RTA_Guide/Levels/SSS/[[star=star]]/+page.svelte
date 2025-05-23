<script>
    import { page } from "$app/state";
    import YouTubeVideo from "components/YouTubeVideo.svelte";

    const STARS = [
        "Red Coin Star",
        "Slide Star",
        "SSS Replica"
    ];

    let star = $derived(Number(page.params.star));
    let route = $derived.by(() => {
        const split = page.url.pathname.split('/');
        return split[split.length - 1];
    });
</script>

<h1>RTA Guide/Sandy Slide Secret</h1>

<p>
    Sandy Slide Secret is the second secret stage of Super Mario Star Road. It is located in a hole above the chandelier inside the castle. Key 1 is required to enter this level.
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
{:else if star === 2}
    <h3>Beginner</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/QbiY2jvI__o?si=6s56Zbt-TAVi7lT6"></YouTubeVideo>

    <h3>Intermediate</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/_ie3JCKEv-E?si=TWV-FmoAfixEYhFh"></YouTubeVideo>
    <YouTubeVideo src="https://www.youtube.com/embed/oIkZe88uvp0?si=8_rgBKPYY8_0eTSE"></YouTubeVideo>

    <h3>Advanced</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/7d3R2bbP3RQ?si=UrDr8aILBkkZ_mx-"></YouTubeVideo>
{:else if star === 3}
    <h3>Beginner</h3>
{/if}
