<script>
    import { page } from "$app/state";
    import YouTubeVideo from "components/YouTubeVideo.svelte";

    const STARS = [
        "Climb to the Highest Pole",
        "Swim Into the Flooded Cage",
        "The Underwater Maze",
        "Break Into the Building",
        "The Chuckya's Red Coins+100 Coins",
        "The Other Entrance"
    ];

    let star = $derived(Number(page.params.star));
    let route = $derived.by(() => {
        const split = page.url.pathname.split('/');
        return split[split.length - 1];
    });
</script>

<h1>RTA Guide/Chuckya Harbor</h1>

<p>
    Chuckya Harbor is the 4th main stage of Super Mario Star Road. It is located outside the castle, between Bowser's Slippery Swamp and Sky Land Resort. 8 Stars are required to enter this level.
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
    <YouTubeVideo src="https://www.youtube.com/embed/Om7-UlUh-DU?si=5fDcs7kz0375PhZ9"></YouTubeVideo>

    <h3>Intermediate</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/VIJivo74QkY?si=rzQYbYY3QTexhDT-"></YouTubeVideo>

    <h3>Advanced</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/nvPjf-kCZqc?si=V1R8ZIvv3-XhlacL"></YouTubeVideo>
{:else if star === 2}
    <h3>Beginner</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/4xmh2iBSHIg?si=xkrQGCOU-j7uxwBq"></YouTubeVideo>

    <h3>Advanced</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/7LlkUqd2E9g?si=4bAZUzorfJyp0LGD"></YouTubeVideo>
{:else if star === 3}
    <h3>Beginner</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/Fe0WkEHn5NU?si=1jk46qM5abPxS6XR"></YouTubeVideo>

    <p>
        <em>The box is only active on acts 1 and 2.</em>
    </p>

    <h3>Intermediate/Advanced</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/k6uyIf2kvj8?si=gCZK4FEpq-rd67Bs"></YouTubeVideo>
{:else if star === 4}
    <YouTubeVideo src="https://www.youtube.com/embed/rm1zuu7uwow?si=qmCN0pCXjQ-fq19j"></YouTubeVideo>
{:else if star === 5}
    <h3>Beginner</h3>
{:else if star === 6}
    <h3>Classic movement</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/6tyonpHbs_0?si=LVcMCDVo_9GRMOAY"></YouTubeVideo>

    <h3>Alternative movement</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/7KtuG7xZOiY?si=cFgKHaFOgGCjnW8L"></YouTubeVideo>
{:else if star === 7}
    <h3>Beginner</h3>
{/if}
