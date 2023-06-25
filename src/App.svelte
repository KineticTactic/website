<script>
    import { onMount } from "svelte";
    import { fade, fly } from "svelte/transition";
    import { flip } from "svelte/animate";
    import Socials from "./lib/Socials.svelte";
    import Navbar from "./lib/Navbar.svelte";
</script>

<main>
    <!-- <Navbar /> -->
    <div class="container">
        <div class="heading-container">
            <h1>
                Hey, i am <span class="highlight">kinetic.</span>
            </h1>
        </div>

        <div class="sub-heading">A 16 year-old full-stack developer. I like to explore various creative ideas through coding.</div>

        <Socials />
    </div>
</main>

<style>
    .heading-container {
        display: flex;
        width: 100%;
        margin: 20vh auto 0 auto;
    }

    h1 {
        display: inline-block;

        font-family: "Raleway", sans-serif;
        font-weight: 400;
        font-size: 4.4rem;
        letter-spacing: -0.015em;
        text-align: center;

        line-height: 1.2;
        margin: 0 auto;
        padding: 1rem 0;

        position: relative;

        --width: 300px;
    }

    h1::before {
        content: "";
        display: block;
        width: var(--width);
        height: 1px;
        position: absolute;
        top: 4rem;
        left: calc(0px - var(--width) - 20px);
        background-color: white;
    }

    h1::after {
        content: "";
        display: block;
        width: var(--width);
        height: 1px;
        position: absolute;
        top: 4rem;
        right: calc(0px - var(--width) - 20px);
        background-color: white;
    }

    .highlight {
        color: #a660ff;
        text-shadow: 0px 0px 15px rgba(166, 96, 255, 0.5);
    }

    .sub-heading {
        width: 40ch;
        margin: 0 auto;

        font-family: "Raleway";
        font-style: normal;
        font-weight: 300;
        font-size: 1.6rem;
        line-height: 2.2rem;
        letter-spacing: -0.015em;
        text-align: center;

        color: #c8c8c8;
    }

    /* media query */
    @media (max-width: 768px) {
        .heading-container {
            flex-direction: column;
        }

        h1 {
            font-size: 3.4rem;
        }

        .sub-heading {
            width: 100%;
        }
    }

    /* media query */
    @media (max-width: 417px) {
        .heading-container {
            display: flex;
            margin: 20vh auto 0 auto;
        }
    }
</style>
