<script lang="ts">
    let { buttonText, href = '/', onclick } = $props()
</script>

<style>
    .button {
        background-color: var(--background-color, #FF8C00);
        width: var(--width, 180px);
        height: 48px;
        border: 2px solid black;
        border-radius: 16px;
        margin-top: var(--margin-top);
        margin-bottom: var(--margin-bottom);
        padding-inline: var(--padding-inline);
        display: flex;
        justify-content: center;
        align-items: center;
        text-decoration: none;
        color: black;
        font-size: 20px;
        font-family: 'Lato', sans-serif;
    }
</style>

<a class="button" {href} on:click={onclick}>
    {buttonText}
</a>