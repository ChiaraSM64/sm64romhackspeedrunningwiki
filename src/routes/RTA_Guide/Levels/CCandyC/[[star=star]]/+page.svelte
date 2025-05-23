<script>
    import { page } from "$app/state";
    import YouTubeVideo from "components/YouTubeVideo.svelte";

    const STARS = [
        "Tuxie Race Down the Slide",
        "Top of the Toy Tower",
        "Door-Knocking",
        "Moving Target",
        "Pole-Jumping",
        "Playful Red Coins+100 Coins"
    ];

    let star = $derived(Number(page.params.star));
    let route = $derived.by(() => {
        const split = page.url.pathname.split('/');
        return split[split.length - 1];
    });
</script>

<h1>RTA Guide/Colossal Candy Clutter</h1>

<p>
    Colossal Candy Clutter is the 11th main stage of Super Mario Star Road. It is located in a toy box in the second floor of the castle. Key 1 and Key 2 are required to access this level.
</p>

<h2>Stars</h2>

<ol>
    {#each STARS as s, i}
        <li class:active={star === i + 1}><a href="{isNaN(star) ? `${route}/` : ''}{i + 1}">{s}</a></li>
    {/each}
</ol>

<h2>{STARS[star - 1]}</h2>

{#if star === 1}
    <YouTubeVideo src="https://www.youtube.com/embed/PPQC-glymb8?si=ckEPC6IpvlDkXn08"></YouTubeVideo>
{:else if star === 2}
    <h3>Beginner</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/U49Ha3Ik8XI?si=zMNFVBw09WcI7GQ7"></YouTubeVideo>

    <h3>Intermediate</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/ey76TvbH6Wg?si=1_WJwKQTI0YC1dwT"></YouTubeVideo>
{:else if star === 3}
    <YouTubeVideo src="https://www.youtube.com/embed/_EFL2TtbVWU?si=GeT-dL7dw7mLP5S3"></YouTubeVideo>
{:else if star === 4}
    <h3>Beginner</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/ZIVQTGT6-aQ?si=IH7CIQKdpbj4UDKf"></YouTubeVideo>

    <h3>Intermediate</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/30ApStNVWLc?si=XLv5ohasAHzrn88L"></YouTubeVideo>
{:else if star === 5}
    <YouTubeVideo src="https://www.youtube.com/embed/V0j53ThnRkI?si=MLxGvZPakrxvPuH8"></YouTubeVideo>
{:else if star === 6}
    <h3>Beginner</h3>
{:else if star === 7}
    <h3>Beginner</h3>
{/if}
