<script>
    import { page } from "$app/state";
    import YouTubeVideo from "components/YouTubeVideo.svelte";

    const STARS = [
        "The Angry Sun's Pyramid Climb",
        "Sandy Race With Koopa the Quick",
        "Ancient Treasure Inside the Pyramid",
        "8 Rocky Red Coins+100 Coins",
        "Glide from the Quicksand Tornado",
        "Sinky Spiral Cave",
    ];

    let star = $derived(Number(page.params.star));
    let route = $derived.by(() => {
        const split = page.url.pathname.split('/');
        return split[split.length - 1];
    });
</script>

<h1>RTA Guide/Koopa Canyon</h1>

<p>
    Koopa Canyon is the 7th main stage of Super Mario Star Road. It is located in the castle sewer behind the 30 Star door. 30 Stars and Key 1 are required to enter this level.
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
    <YouTubeVideo src="https://www.youtube.com/embed/ETjBJuK8OqA?si=F-Ivujla85KHM1h9"></YouTubeVideo>

    <h3>Advanced/Expert</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/RJJy-RXfUis?si=w-SfUtFQ9FN14a_8"></YouTubeVideo>
{:else if star === 2}
    <h3>Beginner</h3>
{:else if star === 3}
    <h3>Beginner</h3>
{:else if star === 4}
    <h3>Beginner</h3>
{:else if star === 5}
    <h3>Beginner</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/IJBpamCuxZk?si=XWUOj7SkLsXzF0CN"></YouTubeVideo>

    <h3>Intermediate</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/s-9zul2NuVM?si=E-fJ8v-Oxh6M9Yd9"></YouTubeVideo>

    <h3>Advanced</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/WP5BZ_g3UKs?si=UwBY6MXtIyTQw8eJ"></YouTubeVideo>

    <p>
        <em>Note that framewalk is not hard at all if you bind any button or DPad Up as Left-Stick Up as your 2nd input. Not every controller plugin has this sadly,
        so you should do the beginner strat if you don't want to change your controller plugin.</em>
    </p>
{:else if star === 6}
    <YouTubeVideo src="https://www.youtube.com/embed/ueh-_PXGjpA?si=nemNvvj8VtuNB2xE"></YouTubeVideo>
{:else if star === 7}
    <h3>Beginner</h3>
{/if}
