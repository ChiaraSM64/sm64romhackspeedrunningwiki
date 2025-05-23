<script>
    import { page } from "$app/state";
    import YouTubeVideo from "components/YouTubeVideo.svelte";

    const STARS = [
        "The Piano-Playing Thwomps",
        "Mouth of the Giant Flute",
        "Tricky Tambourine Trick",
        "Crazy Note Climb",
        "The 8 Musical Red Coins+100 Coins",
        "To Strum the Guitar...",
    ];

    let star = $derived(Number(page.params.star));
    let route = $derived.by(() => {
        const split = page.url.pathname.split('/');
        return split[split.length - 1];
    });
</script>

<h1>RTA Guide/Mad Musical Mess</h1>

<p>
    Mad Musical Mess is the 9th main stage of Super Mario Star Road. It is located inside the castle, in the giant book behind a star door. 30 Stars and Key 1 are required to enter this level.
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
    <YouTubeVideo src="https://www.youtube.com/embed/PeY0I-a1_jk?si=BT8oDt6uRPif_-5d"></YouTubeVideo>

    <h3>Intermediate</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/wfHgU4FStfw?si=XkOUyFA03aGn4byQ"></YouTubeVideo>
{:else if star === 2}
    <h3>Newbie</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/es6cv2_Nxs4?si=SXW1G0EYcRRLDLPc"></YouTubeVideo>

    <h3>Beginner</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/A6hasLg-U1U?si=XeLNzHOpOwAqWvsM"></YouTubeVideo>

    <h3>Intermediate</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/TwLDnjoCJug?si=4aFS53YTYUV9Kf8U"></YouTubeVideo>
{:else if star === 3}
    <h3>Beginner</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/Yy371zOzvEM?si=N5qt4rxV9kt50GdP"></YouTubeVideo>

    <h3>Intermediate/Advanced</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/IXww6Kdb8L8?si=nEeHtacK-MH-0OFD"></YouTubeVideo>
{:else if star === 4}
    <YouTubeVideo src="https://www.youtube.com/embed/olK3PW51CI0?si=PoCsNerZuNRYomvD"></YouTubeVideo>
{:else if star === 5}
    <h3>Beginner</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/41i7kp-wrwM?si=nwZcZw_pWUsCM9bN"></YouTubeVideo>

    <h3>Intermediate</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/qqCKoxI1ln0?si=4ytoCpSm7i-6c0Ie"></YouTubeVideo>
{:else if star === 6}
    <h3>Beginner</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/Lc-rhxdUVwA?si=kMcj4oWiytTBxCjD"></YouTubeVideo>

    <h3>Intermediate</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/bSYE_rcvR_I?si=1xaXOMOyJS66VJaT"></YouTubeVideo>
{:else if star === 7}
    <h3>Beginner</h3>
{/if}
