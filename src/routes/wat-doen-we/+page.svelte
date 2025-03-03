<script lang="ts">
    import Accordion from "$lib/components/Accordion.svelte";
    import Heading from "$lib/components/Heading.svelte";
</script>

<style>

</style>

<Heading headingOne="Ismira" headingTwo="Wat doen we?"/>

<Accordion 
    icon="defaultIcon"
    title="Default Title" 
    text="Default Text"
    providers={["Ismigul", "Samira"]}/>
