<script lang="ts">
    let { paragraphText } = $props()
</script>

<style>
    p {
        padding-top: 30px;
        margin: 0px;
        font-size: 20px;
        font-family: lato;
        text-align: center;
    }
</style>

<p>
    {@html paragraphText}
</p>