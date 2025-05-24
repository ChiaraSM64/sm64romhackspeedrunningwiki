<script>
    import { page } from "$app/state";
    import YouTubeVideo from "components/YouTubeVideo.svelte";

    const STARS = [
        "Climb the Ruins",
        "The Flooded Cave",
        "8 Red Coins of the Pond+100 Coins",
        "Shoot to the Tower Top",
        "Underwater Metal Dash",
        "The Owl's Dinner Time",
    ];

    let star = $derived(Number(page.params.star));
    let route = $derived.by(() => {
        const split = page.url.pathname.split('/');
        return split[split.length - 1];
    });
</script>

<h1>RTA Guide/Piranha Plant Pond</h1>

<p>
	Piranha Plant Pond is the 3rd main course in Super Mario Star Road. It is located near the spawn in a green pipe in the middle of a tiny garden. No stars are required to enter this level.
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
    <YouTubeVideo src="https://www.youtube.com/embed/aYhk_rC8yMY?si=MmE736P97iHxKxSg"></YouTubeVideo>

    <h3>Intermediate</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/f2hB_yjwyiE?si=FQ6uhnLX3yHSLEdr"></YouTubeVideo>
{:else if star === 2}
    <h3>Classic strat</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/ANaa8xncjs0?si=ESGrqgEw0Bc04Y02"></YouTubeVideo>

    <h3>Backup strat</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/Zvtcqg1dlUw?si=LJW85CY8zIHloTed"></YouTubeVideo>
{:else if star === 3}
    <h3>Beginner</h3>
{:else if star === 4}
    <h3>Beginner</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/SiQ0HdmyWc8?si=h2L14za6xhe871Bt"></YouTubeVideo>

    <h3>Intermediate</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/14wf2zlvfoU?si=OOotLs3fDi56G-C5"></YouTubeVideo>

    <h3>Advanced</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/LYTEaQ8SSfA?si=wzaO9h2jB4wMjOUt"></YouTubeVideo>
{:else if star === 5}
    <h3>Beginner</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/NTaOIWY6h_I?si=lB67-fH7pp8EwPXg"></YouTubeVideo>

    <h3>Intermediate</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/ON8RmRnNCeQ?si=DgUSj-icQ5Fx0LCc"></YouTubeVideo>

    <h3>Advanced</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/_jwNo0MjGl8?si=wjhZTGZxlgM_a_Hx"></YouTubeVideo>
    <YouTubeVideo src="https://www.youtube.com/embed/I-ol71z6dOA?si=nRxiQwPuBip6O94Z"></YouTubeVideo>

    <h3>Expert</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/OAXubKZCq-Q?si=6WAR8wfIizprNx--"></YouTubeVideo>
{:else if star === 6}
    <h3>Beginner</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/6yUCrnT41eE?si=ZOJd7firi7mwsXuB"></YouTubeVideo>

    <h3>Intermediate</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/UTDjp0s2HSM?si=ycvG1DrP48qPN1au"></YouTubeVideo>

    <h3>Advanced</h3>
    <YouTubeVideo src="https://www.youtube.com/embed/_ipX1m9YUAo?si=LPOm549sSm2Pu3yf"></YouTubeVideo>
{:else if star === 7}
    <h3>Beginner</h3>
{/if}
