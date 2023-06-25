<script>
    import { onMount } from "svelte";

    export let name;
    export let url;

    let component = null;

    onMount(async () => {
        component = (await import(`./icons/${name}.svelte`)).default;
        console.log(component);
    });
</script>

<a href={url} class="social-button">
    {#if component != null}
        <svelte:component this={component} />
    {/if}
</a>

<style>
    .social-button {
        display: flex;
        align-items: center;
        justify-content: center;
        width: 4.5rem;
        height: 4.5rem;
        /* height: 2rem; */
        border-radius: 50%;
        background-color: #1d1c20;
        /* border: 1px solid #464343; */
        padding: 0.6rem;
        color: #fff;
        fill: #fff;
        text-decoration: none;
        transition: all 0.2s;

        /* insert drop shadow */
        box-shadow: 0px 0px 15px rgba(0, 0, 0, 0.5);
    }

    .social-button:hover {
        background-color: #fff;
        fill: #000;
    }

    /* media query */
    @media (max-width: 768px) {
        .social-button {
            width: 3.5rem;
            height: 3.5rem;
        }
    }
</style>
