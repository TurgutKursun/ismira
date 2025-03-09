<script lang="ts">
    import Heading from "$lib/components/Heading.svelte";
    import TeamMember from "$lib/components/TeamMember.svelte";
</script>

<style>
    .team {
        padding-top: 10px;
        display: flex;
        flex-direction: column;
        gap: 32px;
    }
</style>

<Heading headingOne="Ismira" headingTwo="Wie is wie?"/>

<div class="team">
    <TeamMember img="Ismigul" firstName="Ismigul" lastName="Kursun" position="Klinisch Psychologe"/>
    <TeamMember img="Samira" firstName="Samira" lastName="Zerrouk" position="Klinisch Psychologe"/>
    <div></div>
</div>
