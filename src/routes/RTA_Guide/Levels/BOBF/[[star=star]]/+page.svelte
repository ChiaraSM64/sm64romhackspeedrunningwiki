<script>
    import { page } from "$app/state";
    import YouTubeVideo from "components/YouTubeVideo.svelte";

    const STARS = [
        "Top of the Factory",
        "Wall Kick Up the Tower",
        "Careful Crane Clamber",
        "Swirly Suction Wall",
        "The Rusty Red Coins+100 Coins",
        "The Engine Leak"
    ];

    let star = $derived(Number(page.params.star));
    let route = $derived.by(() => {
        const split = page.url.pathname.split('/');
        return split[split.length - 1];
    });
</script>

<h1>RTA Guide/Bob-Omb Battle Factory</h1>

<p>
    Bob-Omb Battle Factory is the 14th main stage of Super Mario Star Road. It is located above the castle, on the star road in a pipe. Key 1, Key 2 and 65 Stars are required to enter this star since the cannon open at 65 Stars.
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
    <YouTubeVideo src="https://www.youtube.com/embed/k2MoElOzYqM?si=92oPfhLLTWmCsUbC"></YouTubeVideo>

    <h3>Advanced</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/QnFlsg2-q1Y?si=RTOhVwyshoV8itfp"></YouTubeVideo>
{:else if star === 2}
    <h3>Beginner</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/3UKCca4mEJg?si=Z61pV3o-WFUOywFK"></YouTubeVideo>
{:else if star === 3}
    <h3>Beginner</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/_gnDFGYp93M?si=Tly2pY5o1c39qOBy"></YouTubeVideo>

    <h3>Advanced</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/EP3n9sB53MU?si=hjgg784l6FC3dGd4"></YouTubeVideo>
{:else if star === 4}
    <h3>Beginner</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/eZOqYKieHxY?si=5Znw470YN2XGSPWt"></YouTubeVideo>

    <h3>Advanced</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/L44sjsE-MbU?si=FT2XTVns47rnPowb"></YouTubeVideo>
{:else if star === 5}
    <h3>Beginner</h3>
{:else if star === 6}
    <h3>Beginner</h3>
{:else if star === 7}
    <h3>Beginner</h3>
{/if}
