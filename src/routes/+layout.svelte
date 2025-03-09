<script lang="ts">
    import Sidebar from "$lib/components/Sidebar.svelte";
    import { page } from '$app/state';

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
        background-image: linear-gradient(white, #EDCFB0 100%);
        min-height: 100vh;
        padding-bottom: 0;
    }
</style>

<div class="root-container">
    <Sidebar/>
    {@render children()}
</div>

