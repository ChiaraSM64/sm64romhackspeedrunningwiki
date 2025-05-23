<script>
    import { page } from "$app/state";
    import YouTubeVideo from "components/YouTubeVideo.svelte";

    const STARS = [
        "Deep Dive Through the Coral",
        "Boat Ride Among the Rocks",
        "Break Through the Floor",
        "Precision Swimming",
        "Red Coins of the Deep+100 Coins",
        "The 'X' Marks the Spot"
    ];

    let star = $derived(Number(page.params.star));
    let route = $derived.by(() => {
        const split = page.url.pathname.split('/');
        return split[split.length - 1];
    });
</script>

<h1>RTA Guide/Colorful Coral Caverns</h1>

<p>
    Colorful Coral Caverns is the 6th main stage of Super Mario Star Road. It is located in the castle's sewer in a giant pipe. Key 1 is required to enter this level.
</p>

<h2>Stars</h2>

<ol>
    {#each STARS as s, i}
        <li class:active={star === i + 1}><a href="{isNaN(star) ? `${route}/` : ''}{i + 1}">{s}</a></li>
    {/each}
</ol>

<h2>{STARS[star - 1]}</h2>

{#if star === 1}
    <h3>Classic Strat</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/Iw0dSI1aEcU?si=UzIBUm6e0ygWuWSu"></YouTubeVideo>

    <h3>Easier Clip</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/thqts3MbsbY?si=xfihUyP2Y9PUZfPf"></YouTubeVideo>
{:else if star === 2}
    <h3>Beginner</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/6d7cfQ6bwyI?si=ub2ELaDg0FU6aYjO"></YouTubeVideo>

    <h3>Intermediate</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/bmk58fkntYQ?si=X3xaWUv9lZoZv8i_"></YouTubeVideo>
{:else if star === 3}
    <h3>Beginner (no cannon opening)</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/JHysM3XxsCw?si=bA08cSTmJRk5f9sZ"></YouTubeVideo>

    <h3>Intermediate</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/_M56FsfYrzg?si=WkOEtiUls_OgFjwd"></YouTubeVideo>
{:else if star === 4}
    <h3>Classic Strat</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/B38ZKE6I26o?si=konYZMREb59g6G92"></YouTubeVideo>

    <h3>Easier Clip</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/ixgtGqhsRvs?si=mMU-3F1Sjr1wTidG"></YouTubeVideo>
{:else if star === 5}
    <h3>Beginner</h3>
{:else if star === 6}
    <YouTubeVideo src="https://www.youtube.com/embed/jPVE_6LV2Gw?si=r6_AXnQOvphAiReW"></YouTubeVideo>
{:else if star === 7}
    <h3>Beginner</h3>
{/if}
