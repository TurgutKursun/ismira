<script lang="ts">
    import Button from "./Button.svelte";
    import Paragraph from "./Paragraph.svelte";

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
        margin-left: 10px
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
    <span class="material-icons-outlined">diversity_1</span>
    <h2>Therapie</h2>
    {#if open}
    <button class="toggle-btn" on:click={toggle}>
        <span class="material-icons-outlined">remove</span>
    </button>
    {:else}
    <button class="toggle-btn" on:click={toggle}>
        <span class="material-icons-outlined">add</span>
    </button>
    {/if}
</div>

{#if open}
    <div class="accordion-body">
        <Paragraph 
        paragraphText="Lorem Ipsum is simply dummy text of the printing and  typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type."
        --text-align="left"
        --padding-top=0px
        --padding-bottom=0px
        />
    </div>

    <div class="providers">
        {#each providers as provider}
            <Button 
            buttonText={provider}
            --width="fit-content"
            --padding-inline=10px
            />
        {/each}
    </div>
{/if}