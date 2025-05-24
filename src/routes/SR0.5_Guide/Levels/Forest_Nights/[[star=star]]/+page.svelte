<script>
    import { page } from "$app/state";
    import YouTubeVideo from "components/YouTubeVideo.svelte";

    const STARS = [
        "Follow the Path",
        "Walljump Lessons v2",
        "The Great Waterfall",
        "Secrets of the Highest Flowers",
        "Red Coins Between Trees+100 coins",
        "Fly over the Woods"
    ];

    let star = $derived(Number(page.params.star));
    let route = $derived.by(() => {
        const split = page.url.pathname.split('/');
        return split[split.length - 1];
    });
</script>

<h1>RTA Guide/Forest Nights</h1>

<p>
    Forest Nights is the first stage of Star Revenge 0.5: Unused Levels. It is located XX. No stars are required to enter this level.
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
    <YouTubeVideo src="https://youtube.com/embed/29O0wCP6TuE?si=CySykVArdLbcdxHj"></YouTubeVideo>
{:else if star === 2}
    <h3>Beginner</h3>
    <YouTubeVideo src="https://youtube.com/embed/S-RwgQosJAQ?si=T6lNlde6LJ-uDCFo"></YouTubeVideo>
{:else if star === 3}
    <h3>Beginner</h3>
    <YouTubeVideo src="https://youtube.com/embed/tzdsFDHB8sk?si=mGNdelQbcu_2wMy3"></YouTubeVideo>
{:else if star === 4}
    <h3>Beginner</h3>
    <YouTubeVideo src="https://youtube.com/embed/RSsLmbmRu0E?si=8T2nNyX4m6KxEJaX"></YouTubeVideo>
{:else if star === 5}
    <h3>Beginner</h3>
    <YouTubeVideo src="https://youtube.com/embed/YPB9Q5xI9sk?si=_B0JqMST1wzyE75c"></YouTubeVideo>
{:else if star === 6}
    <h3>Beginner</h3>
    <YouTubeVideo src="https://youtube.com/embed/b4bklKR8x2A?si=NI-yq0wYfgv98r_0"></YouTubeVideo>
{:else if star === 7}
    <h3>Beginner</h3>
{/if}
