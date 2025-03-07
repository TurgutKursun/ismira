<script lang="ts">
    import { cubicInOut } from "svelte/easing";
    import Button from "./Button.svelte";
    import Paragraph from "./Paragraph.svelte";
    import { slide } from 'svelte/transition';
    import Icon from "./Icon.svelte";

    let open = false;

    function toggle() {
        open = !open;
    }
</script>

<style>
    .icon {
        margin-top: 28px;
        margin-left: 15px;
    }

    button {
        background-color: transparent;
        border: 0px;
    }

    .sidebar {
        position: fixed;
        top: 0;
        left: 0;
        background-color: #efefef;
        width: 75%;
        height: 100vh;
        display: flex;
        flex-direction: column;
        align-items: center;
        border-right: 2px solid black;
        z-index: 1000;
    }

    .cross {
        align-self: flex-end;
        margin-right: 15px;
    }
</style>

<button class="menu" on:click={toggle}>
    <div class="icon">
        <Icon icon="menu"/>
    </div>
</button>

{#if open}
    <div class="sidebar" transition:slide={{ axis: 'x' , duration: 300, easing: cubicInOut}}>
        <button class="cross" on:click={toggle}>
            <div class="icon">
                <Icon icon="close"/>
            </div>
        </button>
        <Paragraph paragraphText="Menu" --margin-top=200px/>
        <Button buttonText="Home" href="/" --margin-top=20px/>
        <Button buttonText="Afspraak maken" href="/afspraak-maken" --margin-top=20px/>
        <Button buttonText="Wat doen we?" href="/wat-doen-we" --margin-top=20px/>
        <Button buttonText="Wie is wie?" href="/wie-is-wie" --margin-top=20px/>
    </div>
{/if}
