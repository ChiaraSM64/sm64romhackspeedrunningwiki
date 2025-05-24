<script>
    import { page } from "$app/state";
    import YouTubeVideo from "components/YouTubeVideo.svelte";

    const STARS = [
        "BRRC First Star",
        "BRRC Replica",
        "Boss Entry",
        "Boss Fight"
    ];

    let star = $derived(Number(page.params.star));
    let route = $derived.by(() => {
        const split = page.url.pathname.split('/');
        return split[split.length - 1];
    });
</script>

<h1>RTA Guide/Bowser's Retro Remix Castle</h1>

<p>
    Bowser's Retro Remix Castle is located in the castle's basement in the Super Mario World looking castle.
    40 stars are needed to access it without the use of the BLJ strat.
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
    <YouTubeVideo src="https://www.youtube.com/embed/2QdcxBJXM_A?si=Wov2FcJf0OU2jqES"></YouTubeVideo>

    <h3>Intermediate</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/G5YOsJeuSZY?si=sXYdLVHTaD4www3W"></YouTubeVideo>
{:else if star === 2}
    <h3>Intermediate</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/n3Iy9-Vc_n0?si=SJ1K8eJZfGcuDfk9"></YouTubeVideo>
{:else if star === 3}
    <h3>Beginner</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/C7jPRsQtA8E?si=qOJO2-zduO3690od"></YouTubeVideo>

    <h3>Intermediate</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/n3Iy9-Vc_n0?si=SJ1K8eJZfGcuDfk9"></YouTubeVideo>
{:else if star === 4}
    <h3>Beginner/Intermediate</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/_y7FB_MrzGw?si=IGj3QVr3TI-ptfMd"></YouTubeVideo>

    <h3>Alternative starting movements</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/FpADfknieYI?si=7cjE2QYYvUc3W-HM"></YouTubeVideo>

    <h3>Advanced</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/l2tT_ydg0VY?si=B5uyiYQN4A5Ym2H3"></YouTubeVideo>
{/if}
