<script>
    import { page } from "$app/state";
    import YouTubeVideo from "components/YouTubeVideo.svelte";

    const STARS = [
        "The New Whomp King",
        "Climb the Windmill",
        "The Flying Stepping Stones",
        "Finding the Purple Switch",
        "Red Coins of the Sky+100 Coins",
        "Behind the Underwater Gate",
    ];

    let star = $derived(Number(page.params.star));
    let route = $derived.by(() => {
        const split = page.url.pathname.split('/');
        return split[split.length - 1];
    });
</script>

<h1>RTA Guide/Sky Land Resort</h1>

<p>
    Sky Land Resort is the second main stage of Super Mario Star Road. It is located outside the castle next to Chuckya Harbor. No stars are required to enter this level.
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
    <YouTubeVideo src="https://www.youtube.com/embed/vh36UrZozFQ?si=cqMJ2HU5hupygP2l"></YouTubeVideo>

    <h3>Advanced</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/GK9HpEuSxaA?si=yRBlfGmNSZ9FWpLE"></YouTubeVideo>
{:else if star === 2}
    <h3>Beginner</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/qTRI-NP0XAs?si=mVKfvq8e3r6aiDHk"></YouTubeVideo>

    <h3>Intermediate</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/-NhWtEqhgc8?si=T_f0uG8AU4u4yPGp"></YouTubeVideo>

    <h4>Alternative Movements (No windmill clip)</h4>
    <YouTubeVideo src="https://www.youtube.com/embed/P5SFyYoz0ac?si=HOcgLDEEAbcZtu4t"></YouTubeVideo>

    <h3>Advanced</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/X4LPqOvZJ-Q?si=c3FzX9DIrj90t1tR"></YouTubeVideo>
{:else if star === 3}
    <h3>Beginner</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/Vo9QfC_dnZw?si=MoolqInKtqfZYp4D"></YouTubeVideo>

    <h3>Intermediate</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/De8pmhZE_18?si=E1CL65c_d8yX3nOx"></YouTubeVideo>

    <h3>Advanced</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/GW1Nq_O00zM?si=8YlIu3xrzZaJFXWA"></YouTubeVideo>
{:else if star === 4}
    <h3>Beginner</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/ADddzPOqUvY?si=9GXQgcCjLQMGiM53"></YouTubeVideo>

    <h3>Intermediate</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/2qYoq1Kcbrw?si=vD3MO9I_jdsw3l-J"></YouTubeVideo>

    <h3>Advanced</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/stFbu0in3dU?si=KY7-o0HtPexJXKan"></YouTubeVideo>
{:else if star === 5}
    <h3>Beginner</h3>
{:else if star === 6}
    <h3>Beginner/Intermediate</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/ciMqI9HkgME?si=b6FjA5-zdJLAq4Vk"></YouTubeVideo>

    <h3>Advanced</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/iJbs3QkokEI?si=pDH5V97N0nKYC33G"></YouTubeVideo>
{:else if star === 7}
    <h3>Beginner</h3>
{/if}
