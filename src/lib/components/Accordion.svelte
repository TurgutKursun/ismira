<script lang="ts">
    import { fade, slide } from "svelte/transition";
    import Button from "./Button.svelte";
    import Paragraph from "./Paragraph.svelte";
    import { cubicInOut } from "svelte/easing";
    import Icon from "./Icon.svelte";

    let { icon, title, text, providers } = $props()
    let open = $state(false);

    function toggle() {
        open = !open;
    }
</script>

<style>
    button {
        background-color: transparent;
        border: 0px;
    }

    .accordion-header {
        display: flex;
        align-items: center;
        padding-inline: 20px;
    }

    .toggle-btn {
        margin-left: auto;
    }

    h2 {
        margin-inline: 16px;
        margin-block: 16px;
        font-weight: normal;
    }

    .accordion-body {
        padding-inline: 20px;
    }

    .providers {
        padding-inline: 20px;
        padding-top: 20px;
        display: flex;
        gap: 10px
    }
</style>

<div class="accordion-header">
    <Icon icon={icon} size=28px/>
    <h2>{title}</h2>
    {#if open}
    <button class="toggle-btn" on:click={toggle}>
        <Icon icon="remove" size=28px/>
    </button>
    {:else}
    <button class="toggle-btn" on:click={toggle}>
        <Icon icon="add" size=28px/>
    </button>
    {/if}
</div>

{#if open}
    <div transition:slide={{ axis: 'y' , duration: 300, easing: cubicInOut}}>
        <div class="accordion-body">
            <Paragraph 
            paragraphText={text}
            --text-align="left"
            --font-weight=300
            --padding-top=0px
            --padding-bottom=0px
            />
        </div>
    
        <div class="providers">
            {#each providers as provider}
                <Button 
                buttonText={provider.firstName}
                href="/teamlid/{provider.firstName}-{provider.lastName}"
                --width="fit-content"
                --padding-inline=10px
                />
            {/each}
        </div>
    </div>
{/if}