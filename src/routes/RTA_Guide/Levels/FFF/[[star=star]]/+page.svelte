<script>
    import { page } from "$app/state";
    import YouTubeVideo from "components/YouTubeVideo.svelte";

    const STARS = [
        "Deep in the Flaming Caverns",
        "Cross the Lava Lake",
        "Metal Mario Meltdown",
        "Climb the Central Lookout",
        "Burning Red Coins+100 Coins",
        "Rusky Ride into the Volcano"
    ];

    let star = $derived(Number(page.params.star));
    let route = $derived.by(() => {
        const split = page.url.pathname.split('/');
        return split[split.length - 1];
    });
</script>

<h1>RTA Guide/Fatal Flame Falls</h1>

<p>
    Fatal Flame Falls is the 11th main stage of Super Mario Star Road. It is located behind the second key door on the right. Key 1 and 2 are required to enter this level.
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
    <YouTubeVideo src="https://www.youtube.com/embed/DHC_YwwE-qE?si=at36OOdBEscl186L"></YouTubeVideo>

    <h3>Intermediate</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/UePMmgo1uAw?si=NRm5mDdgfe9Rp-yZ"></YouTubeVideo>
{:else if star === 2}
    <h3>Beginner</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/T2nAkzJYRDQ?si=uU0m22JM5uSRGM_5"></YouTubeVideo>

    <h3>Intermediate</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/wN3r5dOfaLU?si=nXZKY7EyjKNW31QV"></YouTubeVideo>
{:else if star === 3}
    <h3>Beginner</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/t9fdbTFjSQY?si=qSlJ7uw_zR1SFlJc"></YouTubeVideo>

    <h3>Intermediate</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/aoZOh5NM16w?si=fYH1b3_oCz263xDO"></YouTubeVideo>
{:else if star === 4}
    <h3>Beginner</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/gXarzST5nB4?si=EIqdSgBTgcx10yIZ"></YouTubeVideo>

    <h3>Intermediate</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/2jYQDl2Ca20?si=vB5PIc5A95yPg0Bo"></YouTubeVideo>

    <h3>Advanced</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/AVwQLaHtuS4?si=ON8f5QlO617WDz1s"></YouTubeVideo>
{:else if star === 5}
    <h3>Beginner</h3>
{:else if star === 6}
    <h3>Beginner (Requires Act 6)</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/tk9KHHSPlFU?si=K5ti695KR8qb-vr3"></YouTubeVideo>

    <h3>Intermediate</h3>
    <p>
        <em>No video yet</em>
    </p>

    <p>
        <em>Note that framewalk is not hard at all if you bind any button or DPad Up as Left-Stick Up as your 2nd input. Not every controller plugin has this sadly,
    so you should do the beginner strat if you don't want to change your controller plugin.</em>
    </p>
{:else if star === 7}
    <h3>Beginner</h3>
{/if}
