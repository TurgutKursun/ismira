<script lang="ts">
    import { page } from '$app/state';
    import TeamMemberDetailed from '$lib/components/TeamMemberDetailed.svelte';
    import { error } from '@sveltejs/kit';
    let firstName = capitalizeFirstLetter(page.params.firstName);
    let lastName = capitalizeFirstLetter(page.params.lastName);

    function capitalizeFirstLetter(val) {
        return String(val).charAt(0).toUpperCase() + String(val).slice(1);
    }
</script>

<style>

</style>

{#if firstName == "Ismigul"}
<TeamMemberDetailed 
    name="Ismigul Kursun"
    position="Klinisch Psychologe" 
    description="Welkom! Ik ben Ismigul Kursun, een Klinisch Psycholoog. Ik ben in de psychologie gestapt omdat iedereen af en toe een luisterend oor nodig heeft. Ik vind het belangrijk dat we samen over moeilijke onderwerpen kunnen praten en oplossingen zoeken." 
    photoFileName="Ismigul" 
    university="Vrije Universiteit Brussel" 
    degree="Master in Klinische Psychologie" 
/>
{:else if firstName == "Samira"}
<TeamMemberDetailed 
    name="Samira Zerrouk"
    position="Klinisch Psychologe" 
    description="Welkom! Ik ben Samira Zerrouk, een Klinisch Psycholoog. Ik ben in de psychologie gestapt omdat iedereen af en toe een luisterend oor nodig heeft. Ik vind het belangrijk dat we samen over moeilijke onderwerpen kunnen praten en oplossingen zoeken." 
    photoFileName="Samira" 
    university="Vrije Universiteit Brussel" 
    degree="Master in Klinische Psychologie" 
/>
{:else}
{error(404, {
    message: 'Teamlid bestaat niet.'
})}
{/if}