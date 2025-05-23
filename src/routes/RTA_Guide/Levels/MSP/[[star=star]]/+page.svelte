<script>
    import { page } from "$app/state";
    import YouTubeVideo from "components/YouTubeVideo.svelte";

    const STARS = [
        "Chilly Lookout Fight",
        "The Snowman's Den",
        "Icy Shell Ride",
        "The Lost Penguin",
        "Cliff Jumping for Red Coins+100 Coins",
        "Glide to the Hidden Ledge",
    ];

    let star = $derived(Number(page.params.star));
    let route = $derived.by(() => {
        const split = page.url.pathname.split('/');
        return split[split.length - 1];
    });
</script>

<h1>RTA Guide/Melting Snow Peaks</h1>

<p>
    Melting Snow Peaks is the 10th main course of Super Mario Star Road. It is located inside the castle, on the right of the staircase. Key 1 is required to enter this level.
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
    <YouTubeVideo src="https://www.youtube.com/embed/SYTsspDztew?si=QOnaAyQJR63ntI3n"></YouTubeVideo>

    <h3>Intermediate/Advanced</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/_hxaCaT6Lsk?si=8dtgaswZ3ipscilM"></YouTubeVideo>
{:else if star === 2}
    <h3>Beginner</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/TwlERTkb25c?si=ArwJRcB5cizpVPgI"></YouTubeVideo>

    <h3>Intermediate</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/i9zPKHMlhlI?si=gb3n1fr0wbFExBqx"></YouTubeVideo>
{:else if star === 3}
    <h3>Beginner/Intermediate</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/ZIDO5_qT4qo?si=GXn3NhcAOib-KuXj"></YouTubeVideo>

    <h3>Advanced</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/2DGLNItx118?si=nVNy-WTJqTnVwoqv"></YouTubeVideo>
{:else if star === 4}
    <h3>Beginner/Intermediate</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/nGGoXAiJjiY?si=NMX8n4umrIpc3_lh"></YouTubeVideo>

    <h3>Advanced</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/_CuorwaYpbQ?si=07uCfx-YJU35xdeW"></YouTubeVideo>
{:else if star === 5}
    <h3>Beginner</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/lUGNq2UJ0kk?si=bbriXtnxSPoXjZ0X"></YouTubeVideo>

    <h3>Advanced</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/LreIq_Vu76w?si=ru7mnGqnxPASMOQE"></YouTubeVideo>
    <YouTubeVideo src="https://www.youtube.com/embed/rF4sVSLxsIg?si=j1qqn58KYArWywTC"></YouTubeVideo>
{:else if star === 6}
    <h3>Beginner</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/l8HPYqbgkZI?si=-zduPOmSLmtQ5wTr"></YouTubeVideo>

    <h3>Intermediate/Advanced</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/yE6bq7VJvI8?si=TnFzAXV93qwcuefD"></YouTubeVideo>
{:else if star === 7}
    <h3>Beginner</h3>
{/if}
