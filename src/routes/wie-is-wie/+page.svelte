<script lang="ts">
    import TeamMember from "$lib/components/TeamMember.svelte";
</script>

<style>
    .team {
        display: flex;
        flex-direction: column;
        gap: 32px;
    }
</style>

<div class="team">
    <TeamMember img="Ismigul" name="Ismigul Kursun" position="Klinisch Psychologe"/>
    <TeamMember img="Samira" name="Samira Zerrouk" position="Klinisch Psychologe"/>
    <div></div>
</div>
