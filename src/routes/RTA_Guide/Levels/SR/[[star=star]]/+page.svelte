<script>
    import { page } from "$app/state";
    import YouTubeVideo from "components/YouTubeVideo.svelte";

    const STARS = [
        "Follow the Glittering Path",
        "Climb Through the Machinery",
        "Shutdown the Handroid",
        "Aim the Turret",
        "Red Coins in the Crater+100 Coins",
        "In the Cage",
    ];

    let star = $derived(Number(page.params.star));
    let route = $derived.by(() => {
        const split = page.url.pathname.split('/');
        return split[split.length - 1];
    });
</script>

<h1>RTA Guide/Starlight Runway</h1>

<p>
    Starlight Runway is the 15th main stage of Super Mario Star Road. It is located above the castle, on the star road, inside the UFO. Key 1, Key 2 and 65 Stars are required since the cannon open at 65 Stars.
</p>

<h2>Stars</h2>

<ol>
    {#each STARS as s, i}
        <li class:active={star === i + 1}><a href="{isNaN(star) ? `${route}/` : ''}{i + 1}">{s}</a></li>
    {/each}
</ol>

<h2>{STARS[star - 1]}</h2>

{#if star === 1}
    <YouTubeVideo src="https://www.youtube.com/embed/lrbORY8iTsk?si=z3L5lzQsZgOGtlxF"></YouTubeVideo>
{:else if star === 2}
    <h3>Beginner (Late Cycle)</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/nIsJeuGeTjg?si=VzeEq4CFtwe3bZ-X"></YouTubeVideo>

    <h3>Intermediate (Half Cycle)</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/3Bl5lLmu3f8?si=1NrLgZ9j_xVNWAm3"></YouTubeVideo>

    <h3>Advanced (Pro Cycle)</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/6gXU6nBXx3E?si=Wm333Mvw9ZTS2_GV"></YouTubeVideo>
{:else if star === 3}
    <h3>Beginner</h3>
{:else if star === 4}
    <h3>Beginner</h3>
{:else if star === 5}
    <h3>Beginner</h3>
{:else if star === 6}
    <YouTubeVideo src="https://www.youtube.com/embed/6IZQa7S6ORM?si=qnPHBjclT2HNKLhX"></YouTubeVideo>
{:else if star === 7}
    <h3>Beginner</h3>
{/if}
