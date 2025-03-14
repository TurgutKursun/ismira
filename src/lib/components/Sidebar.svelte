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

    .closer {
        position: fixed;
        top: 0px;
        left: 75%;
        width: 25%;
        height: 100vh;
    }

    @media (min-width: 768px) {
        .sidebar {
            width: 300px;
        }

        .closer {
            left: 300px;
            width: 100%;
        }
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
        <Button buttonText="Home" onclick={toggle} href="/" --margin-top=20px/>
        <Button buttonText="Contact" onclick={toggle} href="/contact" --margin-top=20px/>
        <Button buttonText="Wat doen we?" onclick={toggle} href="/wat-doen-we" --margin-top=20px/>
        <Button buttonText="Wie is wie?" onclick={toggle} href="/wie-is-wie" --margin-top=20px/>
    </div>

    <button class="closer" aria-label="sidebar-closer" style="margin-inline: 0px; padding-inline: 0px;" on:click={toggle}>
        
    </button>
{/if}
