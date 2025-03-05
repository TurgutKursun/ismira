<script lang="ts">
    import Sidebar from "$lib/components/Sidebar.svelte";

    let { children } = $props()
</script>

<svelte:head>
    <link href="https://fonts.googleapis.com/icon?family=Material+Icons+Outlined" rel="stylesheet">
    <link href="https://fonts.googleapis.com/icon?family=Material+Symbols+Outlined" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display&display=swap" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Lato:wght@300;400;700&display=swap" rel="stylesheet">
</svelte:head>

<style>
    .root-container {
        background-image: linear-gradient(white, white 37%, #EDCFB0 55%, #EDCFB0 100%);
        min-height: 100vh;
    }
</style>

<div class="root-container">
    <Sidebar/>
    {@render children()}
</div>

