<script lang="ts">
    let { buttonText } = $props()
</script>

<style>
    button {
        background-color: #FF8C00;
        width: 180px;
        height: 48px;
        border-radius: 16px;
        border-width: 2px;
        /* ...existing code... */
        margin-top: var(--margin-top);
        margin-bottom: var(--margin-bottom);
        /* ...existing code... */
        display: flex;
        justify-content: center;
        align-items: center;
    }

    p {
        font-size: 20px;
        font-family: 'Lato', sans-serif;
    }
</style>

<button>
    <p>
        {buttonText}
    </p>
</button>