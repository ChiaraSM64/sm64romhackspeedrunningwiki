<script>
    import { page } from "$app/state";
    import YouTubeVideo from "components/YouTubeVideo.svelte";

    const STARS = [
        "Swinging Through the Clouds",
        "Platform Ride to the Cage",
        "Fluffy Castle Climb",
        "The Frozen Cloud",
        "The Giant Thwomp's Treasure",
        "Airborne Red Coins+100 Coins"
    ];

    let star = $derived(Number(page.params.star));
    let route = $derived.by(() => {
        const split = page.url.pathname.split('/');
        return split[split.length - 1];
    });
</script>

<h1>RTA Guide/Cloudrail Station</h1>

<p>
    Cloudrail Station is the 12th main stage of Super Mario Star Road. It is located on the castle second floor in the window. Key 1 and Key 2 are required to enter this level.
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
    <YouTubeVideo src="https://www.youtube.com/embed/fePQg6qksPs?si=J_DHQTY1QFXtHKq7"></YouTubeVideo>

    <h3>Intermediate/Advanced</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/gwglZv_-nso?si=JYI4LhDMDINghZQS"></YouTubeVideo>
{:else if star === 2}
    <h3>Beginner</h3>
{:else if star === 3}
    <h3>Beginner</h3>
{:else if star === 4}
    <h3>Beginner</h3>
{:else if star === 5}
    <h3>Beginner</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/J-vkFV7jAzk?si=dxmsbfU8L4RP4PPD"></YouTubeVideo>

    <h3>Advanced</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/AI5oqWD8F_s?si=4abIdyuCmbMqu9IE"></YouTubeVideo>
{:else if star === 6}
    <h3>Beginner</h3>
{:else if star === 7}
    <h3>Beginner</h3>
{/if}
