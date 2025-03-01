<script lang="ts">
    let { children } = $props()
</script>

<svelte:head>
    <link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display&display=swap" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Lato&display=swap" rel="stylesheet">
</svelte:head>

<style>
    span {
        margin-top: 28px;
        margin-left: 15px;
    }
    .root-container {
        background-image: linear-gradient(white, white 37%, #EDCFB0 55%, #EDCFB0 100%);
        min-height: 100vh;
    }
    :global(body) {
        margin: 0;
        padding: 0;
    }
</style>

<div class="root-container">
    <span class="material-icons">menu</span>
    {@render children()}
</div>

