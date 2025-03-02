<script lang="ts">
    let { buttonText } = $props()
</script>

<style>
    .button {
        background-color: #FF8C00;
        width: 180px;
        height: 48px;
        border: 2px solid black;
        border-radius: 16px;
        /* ...existing code... */
        margin-top: var(--margin-top);
        margin-bottom: var(--margin-bottom);
        /* ...existing code... */
        display: flex;
        justify-content: center;
        align-items: center;
        text-decoration: none;
        color: black;
        font-size: 20px;
        font-family: 'Lato', sans-serif;
    }
</style>

<a class="button" href="/afspraak-maken">
    {buttonText}
</a>