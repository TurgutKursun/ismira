<script lang="ts">
    let { img }: { img: string} = $props()
</script>

<style>
    img {
        clip-path: circle();
        width: 200px;
        background-color: white;
    }
</style>

{#await import(`$lib/images/${img}.png`) then { default: src }}
  <img {src} alt="Profile"/>
{/await}