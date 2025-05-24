<script>
    import { page } from "$app/state";
    import YouTubeVideo from "components/YouTubeVideo.svelte";

    const STARS = [
        "Big Boo's Tower",
        "Top of the Risky Walkway",
        "The Secret Tunnel",
        "The Lone Tree",
        "Haunted Ride For Red Coins+100 Coins",
        "Calm the Angry Eye",
    ];

    let star = $derived(Number(page.params.star));
    let route = $derived.by(() => {
        const split = page.url.pathname.split('/');
        return split[split.length - 1];
    });
</script>

<h1>RTA Guide/Gloomy Garden</h1>

<p>
    Gloomy Garden is the 5th Main Stage. It is located outside the castle between Bob-Omb Islands and Bowser's Slippery Swamp. You need 8 Stars to enter this level without
    the use of any unintended strats.
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
    <YouTubeVideo src="https://www.youtube.com/embed/mR-SIVodqdg?si=SsBs45rDQhzSgSJA"></YouTubeVideo>

    <h3>Intermediate/Advanced</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/niPSyvYNP30?si=JO9fKPQCE6Vh_h7z"></YouTubeVideo>
{:else if star === 2}
    <h3>Newbie</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/6iMky_NHD64?si=yssDga8YI7V9pgCF"></YouTubeVideo>

    <h3>Beginner</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/E0IgelPamcY?si=2TMQyCQZV9Te1JRV"></YouTubeVideo>

    <h3>Intermediate</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/68iIByC25Os?si=mfgqtmqPgVTBMIST"></YouTubeVideo>

    <h3>Advanced</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/oSBlJEI3xEQ?si=FhVVr-SemGcS2jOp"></YouTubeVideo>
{:else if star === 3}
    <h3>Beginner</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/oZeB0xOnncw?si=TIkI5dwgEOKlth30"></YouTubeVideo>

    <h3>Intermediate</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/yNiTZjcGZ8I?si=2Q_G44oTrnC_s1Lq"></YouTubeVideo>
{:else if star === 4}
    <h3>Beginner</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/VxlvogoTU1M?si=AZQWhE6omoBOLq8B"></YouTubeVideo>

    <h3>Intermediate/Advanced</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/E0gE8zYCj4o?si=kSiOfbb6RG4tCD7C"></YouTubeVideo>
{:else if star === 5}
    <h3>Beginner</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/5ivQbQUN68k?si=YFV1mddex5HAWWNn"></YouTubeVideo>

    <p>
        <em>Note that 100c+Reds are by far the hardest stars in the run for a beginner, don't blame yourself if you're not consistent on it.</em>
    </p>

    <h3>Advanced</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/7whRKfSrZss?si=p11VgQwhnYn_7hYb"></YouTubeVideo>
    <YouTubeVideo src="https://www.youtube.com/embed/Oni_SMsAoYo?si=RUs_U6mCgK7ZoxYv"></YouTubeVideo>

    <p>
        <em>Entering Bowser's Slippery Swamp breaks trajectory objects, which includes the Gloomy Garden elevator. So, if you do that level before Gloomy Garden, it will affect the red coin star.
        The "hard red first" route is recommended if the elevator isn't broken. Otherwise use the "right first" route or the "hard red first" route without the elevator (after the 100 coin star,
        jump to the ring platforms and climb the wall).</em>
    </p>
{:else if star === 6}
    <h3>Good RNG</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/MXyfWxZ3MdU?si=jRwatedbFGFSxIVE"></YouTubeVideo>

    <h3>Bad RNG</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/Orva16qJw_U?si=Uw9gVK89ao9lol8J"></YouTubeVideo>
{:else if star === 7}
    <h3>Beginner</h3>
{/if}
