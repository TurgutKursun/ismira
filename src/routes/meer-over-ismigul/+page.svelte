<script lang="ts">
    import { page } from '$app/state';
    import TeamMemberDetailed from '$lib/components/TeamMemberDetailed.svelte';
    import { error } from '@sveltejs/kit';

    function capitalizeFirstLetter(val) {
        return String(val).charAt(0).toUpperCase() + String(val).slice(1);
    }
</script>

<style>

</style>

<TeamMemberDetailed 
    name="Ismigul Kursun"
    position="Klinisch Psychologe" 
    description="Vanuit een diepe interesse in de menselijke psychologie heb ik met succes mijn masteropleiding in de klinische psychologie afgerond aan de Vrije Universiteit Brussel. Tijdens mijn opleiding liep ik stage bij de Brusselse politiezone, waar ik waardevolle ervaring opdeed binnen een complexe context.
Momenteel ben ik werkzaam bij de privékliniek PYZO in Merksem (Antwerpen), waar ik voornamelijk werk met cliënten die te maken hebben gehad met complexe trauma's. Om mijn cliënten nog beter te kunnen ondersteunen, heb ik mij verder gespecialiseerd in EMDR-therapie. Binnen korst start ik in Zaventem (website/contact gegevens en locatie binnen kort beschikbaar)
<br/>
<br/>

U kunt bij mij terecht voor individuele therapie, voor u zelf of u kind (ik werk graag met minderjarigen vanaf 12jaar). Tijdens een eerste intakegesprek bespreken we samen uw hulpvraag en verwachtingen. Op basis daarvan starten we in de daaropvolgende sessies een traject op maat."
    photoFileName="Ismigul" 
    university="Vrije Universiteit Brussel" 
    degree="Master in Klinische Psychologie <br/> </br/> EMDR Integrativa" 
/>