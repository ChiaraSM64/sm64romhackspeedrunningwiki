<script>
    import { page } from "$app/state";
    import YouTubeVideo from "components/YouTubeVideo.svelte";

    const STARS = [
        "BSS First Star",
        "BSS Replica",
        "Boss Entry",
        "Boss Fight"
    ];

    let star = $derived(Number(page.params.star));
    let route = $derived.by(() => {
        const split = page.url.pathname.split('/');
        return split[split.length - 1];
    });
</script>

<h1>RTA Guide/Bowser's Slippery Swamp</h1>

<p>
    Bowser's Slippery Swamp is located between Gloomy Garden (Course 5) and Chuckya Harbor (Course 4) outside the castle.
    20 stars are needed to access it without the use of the door clipping strat.
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
    <YouTubeVideo src="https://www.youtube.com/embed/KRFMsqUMBn0?si=9wfQHnoYyf-2MsfX"></YouTubeVideo>

    <h3>Intermediate</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/ixvQhVQMxck?si=X7gZ47iuJyAxItbP"></YouTubeVideo>
{:else if star === 2}
    <h3>Advanced</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/4-DfVLzCkKE?si=by7ucsIvJMAh2By9"></YouTubeVideo>
{:else if star === 3}
    <h3>Beginner</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/gWQJ3wJVC90?si=uSlZU0-jsNeiKA29"></YouTubeVideo>

    <h3>Intermediate</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/xhZQkR11fpM?si=qCJwbyRQjJzq6K_9"></YouTubeVideo>

    <h3>Advanced</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/X4nIcSgUcp8?si=bb0UNb64nTy21hOK"></YouTubeVideo>

    <h3>Backup</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/HxocmpZJ3cs?si=Z4FkmsvVU4wFJZqE"></YouTubeVideo>
{:else if star === 4}
    <h3>Beginner</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/uFTw-wt7GII?si=F9_orOtEX5uY4zny"></YouTubeVideo>

    <h3>Alternative ending</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/S5pZWfHm-k4?si=_j4Fze_M7uJxA7lE"></YouTubeVideo>

    <h3>Advanced</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/MB8rp-28QnE?si=MV7PHAPl920TF6Qx"></YouTubeVideo>
{/if}
