<script lang="ts">
    let { paragraphText } = $props()
</script>

<style>
    p {
        padding-top: var(--padding-top, 30px);
        padding-bottom: var(--padding-bottom, 30px);
        padding-inline: var(--padding-inline);
        margin: 0px;
        font-size: 20px;
        font-family: lato;
        font-weight: var(--font-weight, 400);
        text-align: var(--text-align, center);
    }
</style>

<p>
    {@html paragraphText}
</p>