<script>
    import { slide } from "svelte/transition";
    let active = $state(false);
</script>

<section>
    <button onclick={() => (active = !active)}>Toggle</button>
    {#if active}
        <ul transition:slide={{ duration: 1000, axis: 'y' }}>
            <li>Item 1</li>
            <li>Item 2</li>
            <li>Item 3</li>
            <li>Item 4</li>
        </ul>
    {/if}
</section>

<style>
    section{
        padding: 2rem;
        background-color: aquamarine;
    }
    ul{
        padding: 1rem;
        background-color: bisque;
        list-style-type: none;
    }
</style>