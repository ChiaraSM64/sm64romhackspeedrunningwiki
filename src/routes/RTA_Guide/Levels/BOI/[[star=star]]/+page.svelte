<script>
    import { page } from "$app/state";
    import YouTubeVideo from "components/YouTubeVideo.svelte";

    const STARS = [
        "Big Bob-omb's Sky Fort",
        "Top of the Sunken Ship",
        "In the Side of the Mountain",
        "Find the 8 Red Coins+100 Coins",
        "Deep Dive in the Cage",
        "Smash the Chain Chomp's Rocks"
    ];

    let star = $derived(Number(page.params.star));
    let route = $derived.by(() => {
        const split = page.url.pathname.split('/');
        return split[split.length - 1];
    });
</script>

<h1>RTA Guide/Bob-Omb Islands</h1>

<p>
    Bob-Omb Islands is the first stage of Super Mario Star Road. It is located outside the castle, next to Gloomy Garden. No stars are required to enter this star.
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
{:else if star === 2}
    <h3>Beginner</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/ImEa3a1E9jo?si=CXLWuD38H6qLU5y9"></YouTubeVideo>
{:else if star === 3}
    <h3>Beginner</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/f1lsvMrZcD0?si=0V_QloEpbvD_5_33"></YouTubeVideo>

    <h3>Intermediate</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/i3jUTo5kUgA?si=5jPcwGU1TDIuZti2"></YouTubeVideo>

    <h3>Advanced</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/_jgoB3C64ss?si=__wmLXVJ8hie8HiN"></YouTubeVideo>

    <h2>Strats with cannon openning</h2>

    <h3>Intermediate/Advanced</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/1OgqcJwyq0k?si=abQCA_N7bjAtoo9J"></YouTubeVideo>
{:else if star === 4}
    <h3>Beginner</h3>
{:else if star === 5}
    <h3>Newbie</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/hsNX2fS4AAQ?si=i2sheOrW_-4vuPnD"></YouTubeVideo>

    <h3>Beginner</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/lymgFoZmgII?si=tCQ-j0M0zD9tOVJd"></YouTubeVideo>

    <h3>Intermediate</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/q2uZxxKKFLw?si=MBrxpfNDo97PHUIx"></YouTubeVideo>

    <h3>Advanced</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/8S0gVgJYKgw?si=yBZDw9S04v_tRHOc"></YouTubeVideo>
{:else if star === 6}
    <h3>Extremely Beginner</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/lzc1xbgxTW0?si=_eOWmPfljFqEXOfh"></YouTubeVideo>

    <h3>Intermediate</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/4HjxRqQJVuI?si=eR2h3PqK8pJOVA4h"></YouTubeVideo>
{:else if star === 7}
    <h3>Beginner</h3>
{/if}
