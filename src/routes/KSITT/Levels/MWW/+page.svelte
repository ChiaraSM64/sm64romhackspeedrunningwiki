<script>
    import { page } from "$app/state";
    import YouTubeVideo from "components/YouTubeVideo.svelte";

    const STARS = [
        "Get on the Kong",
        "Katze's Old House",
        "Sand Pit+60 coins",
        "Usernames's Redesigned Parking Lot",
        "Collect the Restaurant's Tips",
        "Burger in the Oven LMAO"
    ];

    let star = $derived(Number(page.params.star));
    let route = $derived.by(() => {
        const split = page.url.pathname.split('/');
        return split[split.length - 1];
    });
</script>

<h1>RTA Guide/McDonalds World War</h1>

<p>
    McDonalds World War is the 1st main stage of Katze Stuck in the Toilet 64. It is located inside the YOOOOOOOOO. Only 1 Star is required to enter this level as you need it to enter the 2nd overworld.
</p>

<h2>Stars</h2>

<ol>
    {#each STARS as s, i}
        <li class:active={star === i + 1}><a href="{isNaN(star) ? `${route}/` : ''}{i + 1}">{s}</a></li>
    {/each}
</ol>

<h2>{STARS[star - 1]}</h2>

{#if star === 1}
    <YouTubeVideo src=""></YouTubeVideo>
{:else if star === 2}
    <YouTubeVideo src=""></YouTubeVideo>
{:else if star === 3}
    <YouTubeVideo src=""></YouTubeVideo>
{:else if star === 4}
    <YouTubeVideo src=""></YouTubeVideo>
{:else if star === 5}
    <h3>Beginner</h3>
{:else if star === 6}
    <h3>Intermediate</h3>
    <YouTubeVideo src=""></YouTubeVideo>
{:else if star === 7}
    <h3>Beginner</h3>
{/if}