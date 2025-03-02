<script lang="ts">
    let { address } = $props()
</script>

<style>
    a {
        padding-top: var(--padding-top, 30px);
        padding-bottom: var(--padding-bottom, 30px);
        margin: 0px;
        font-size: 20px;
        font-family: lato;
        text-align: center;
    }
</style>

<a href="https://www.google.com/maps/search/?api=1&query={address}">
    {address}
</a>