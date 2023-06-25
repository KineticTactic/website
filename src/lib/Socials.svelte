<script>
    import SocialButton from "./SocialButton.svelte";

    const socials = [
        {
            name: "github",
            url: "https://github.com/KineticTactic",
        },
        {
            name: "twitter",
            url: "https://twitter.com/tactickinetic",
        },
        {
            name: "instagram",
            url: "https://instagram.com/tactickinetic",
        },
        {
            name: "discord",
            url: "https://discordapp.com/users/733608333575192606",
        },
    ];
</script>

<ul class="socials">
    {#each socials as social}
        <li>
            <SocialButton name={social.name} url={social.url} />
        </li>
    {/each}
</ul>

<style>
    .socials {
        display: flex;
        justify-content: center;
        align-items: center;
        /* width: 65%; */
        margin: 2rem auto;
        padding: 1rem 0;
    }

    ul {
        list-style-type: none;
        margin: 0;
        padding: 0;
        overflow: hidden;
    }

    li {
        margin: 0 1.2rem;
    }

    /* media query */
    @media (max-width: 768px) {
        .socials {
            margin: 1rem auto;
        }

        li {
            margin: 0 0.5rem;
        }
    }
</style>
