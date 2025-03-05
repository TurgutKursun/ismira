<script lang="ts">
    let { img }: { img: string} = $props()
</script>

<style>
    img {
        clip-path: circle();
        width: 200px;
    }
</style>

{#await import(`$lib/images/${img}.png`) then { default: src }}
  <img {src} alt="Profile"/>
{/await}