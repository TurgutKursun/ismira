<script lang="ts">
    import Accordion from "$lib/components/Accordion.svelte";
    import Heading from "$lib/components/Heading.svelte";
</script>

<style>
    @media(min-width: 512px) {
        .accordions {
            width: 40%;
            display: flex;
            flex-direction: column;
            margin: 0 auto;
            margin-top: 30px 
        }
    }
</style>

<Heading headingOne="Ismira" headingTwo="Wat doen we?"/>

<div class="accordions">
    <Accordion 
    icon="diversity_1"
    title="Therapie" 
    text="We bieden begeleiding bij psychische moeilijkheden en persoonlijke groei. Samen werken we aan meer welzijn. <br/> <br/> Voor therapie kan u terecht bij:"
    providers={[{
        firstName: "Ismigul",
        lastName: "Kursun"
    }, {
            firstName: "Samira",
            lastName: "Zerrouk"
        }]}
        />

    <Accordion
    icon="toys_and_games"
    title="EMDR"
    text="Met EMDR helpen we bij het verwerken van trauma en ingrijpende ervaringen. Met gerichte technieken verminderen we de emotionele impact van herinneringen. <br/> <br/> Voor EMDR kan u terecht bij:"
        providers={[{
        firstName: "Ismigul",
        lastName: "Kursun"
    }, {
            firstName: "Samira",
            lastName: "Zerrouk"
        }]}
    />

    <Accordion
    icon="person_search"
    title="Diagnostiek"
    text="We voeren psychologische onderzoeken uit om inzicht te krijgen in klachten en sterktes. Dit helpt om de juiste ondersteuning en begeleiding te bieden. <br/> <br/> Voor diagnostiek kan u terecht bij:"
        providers={[{
        firstName: "Ismigul",
        lastName: "Kursun"
    }, {
            firstName: "Samira",
            lastName: "Zerrouk"
        }]}
    />

    <Accordion
    icon="toys_and_games"
    title="Kinderen"
    text="We ondersteunen kinderen bij emotionele en gedragsmatige uitdagingen. We streven naar een veilige omgeving waarin ze zich optimaal kunnen ontwikkelen. <br/> <br/> Voor begeleiding van kinderen kan u terecht bij:"
        providers={[{
        firstName: "Ismigul",
        lastName: "Kursun"
    }, {
            firstName: "Samira",
            lastName: "Zerrouk"
        }]}
    />
</div>
