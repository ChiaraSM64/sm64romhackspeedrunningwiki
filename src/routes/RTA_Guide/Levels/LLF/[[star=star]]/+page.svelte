<script>
    import { page } from "$app/state";
    import YouTubeVideo from "components/YouTubeVideo.svelte";

    const STARS = [
        "A Big Bug Problem",
        "Shining Down From the Tree Tops",
        "Quick Lily Pad Hop",
        "The Bee's Treasure",
        "Vine-Climbing for 8 Red Coins+100 Coins",
        "The Missing Star",
    ];

    let star = $derived(Number(page.params.star));
    let route = $derived.by(() => {
        const split = page.url.pathname.split('/');
        return split[split.length - 1];
    });
</script>

<h1>RTA Guide/Large Leaf Forest</h1>

<p>
    Large Leaf Forest is the 8th main stage of Super Mario Star Road. It is located inside the castle at the left of the staircase. Key 1 is required to enter this level.
</p>

<h2>Stars</h2>

<ol>
    {#each STARS as s, i}
        <li class:active={star === i + 1}><a href="{isNaN(star) ? `${route}/` : ''}{i + 1}">{s}</a></li>
    {/each}
</ol>

<h2>{STARS[star - 1]}</h2>

{#if star === 1}
    <p>
        <em>The wiggler is act 1 only.</em>
    </p>

    <YouTubeVideo src="https://www.youtube.com/embed/nGUQGf1vJTo?si=Nev04HPoo-cIgHdb"></YouTubeVideo>
{:else if star === 2}
    <h3>Act Info</h3>
    <ul>
        <li>Since this star is act 2, only acts 1 and 2 are available before collecting this star.</li>
        <li>Act 2 is required if you're not doing the framewalk strat.</li>
        <li>If doing the framewalk strat, it's recommended to do this star on act 1 since the enemies in the tree will be missing.</li>=
    </ul>

    <h3>Beginner</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/Yxe3skjSzA8?si=L_qn4nWjIht84hAo"></YouTubeVideo>

    <h3>Intermediate</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/us2yD37Qq-Q?si=cR7igrkcdsNHpV_7"></YouTubeVideo>

    <p>
        <em>Note that framewalk is not hard at all if you bind any button or DPad Up as Left-Stick Up as your 2nd input. Not every controller plugin has this sadly,
        so you should do the beginner strat if you don't want to change your controller plugin.</em>
    </p>

    <h3>Advanced</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/sZQKnBU4AOI?si=fA93VQ3tZboGcbe_"></YouTubeVideo>
{:else if star === 3}
    <p>
        <em>The lakitu is missing on act 2.</em>
    </p>

    <h3>Beginner</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/HM48Y_rhWO8?si=Vo28Gz8fros5mWcU"></YouTubeVideo>

    <h3>Advanced</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/FBsdG5IWDY0?si=vxsYQ-wlZxZJB0r2"></YouTubeVideo>
{:else if star === 4}
    <h3>Act Info</h3>
    <ul>
        <li>beehive star: acts 2 to 6</li>
        <li>tree lakitu: acts 2, 5, and 6</li>
        <li>left chuckya: acts 2 to 6</li>
        <li>right chuckya: acts 2, 3, 5, and 6</li>
        <li>beehive's spiny: only act 4</li>
    </ul>
    <p>
        <em>In a fullgame run, only acts 1-4 are available before collecting this star and only acts 2-4 work. Act 4 is best if you are climbing the tree via the mushroom since the right chuckya and
        lakitu will be gone. If doing the framewalk strat, you can use act 3 since the beehive's spiny and lakitu won't be there.</em>
    </p>


    <h3>Beginner</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/GkYJldp3AKs?si=RNCpWee96mwt5ByP"></YouTubeVideo>

    <h3>Intermediate</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/C48QilnTBUk?si=VHngrWO6dUQFMZiy"></YouTubeVideo>

    <p><em>Note that framewalk is not hard at all if you bind any button or DPad Up as Left-Stick Up as your 2nd input. Not every controller plugin has this sadly,
    so you should do the beginner strat if you don't want to change your controller plugin.</em></p>

    <h3>Advanced</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/7VeLjPFOJ18?si=wUsFyAWtGG2fkWcj"></YouTubeVideo>
{:else if star === 5}
    <p>
        <em>Act 1 for this star is bad given the moving mushroom and many tree coins are missing.
        The tree lakitu is active on acts 2, 5, and 6. The right tree chuckya is active on acts 2, 3, 5, and 6.
    </p>
    <p>
        <em>You can use act 3 or 4 so the lakitu doesn't bother you, but act 3 is better so that you can use the right chuckya as backup coins.</em>
    </p>

    <h3>Beginner</h3>
{:else if star === 6}
    <p>
        <em>This star is available on all acts.</em>
    </p>

    <h3>Beginner</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/z2Jsd4KhWsY?si=8iS-NuKft-y4gZwM"></YouTubeVideo>

    <h3>Intermediate</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/qalHozbPyzk?si=OlRbwMYjYUJwBJgm"></YouTubeVideo>
{:else if star === 7}
    <h3>Beginner</h3>
{/if}
