<script>
    import Button from "$lib/components/Button.svelte";
    import Heading from "$lib/components/Heading.svelte";
    import Paragraph from "$lib/components/Paragraph.svelte";
</script>

<style>
    .lottie {
        padding: 0px;
        margin-top: 0px;
        width: 350px;
        margin-inline: auto;
    }
    .buttons {
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    .container {
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    @media (min-width: 768px) {
        .lottie {
            width: 400px;
            display: block;
            margin-inline: auto;
        }

        .buttons {
            display: flex;
            flex-direction: row;
            justify-content: center;
            align-items: center;
            gap: 20px
        }
    }
</style>

<div class="container">
    <Heading headingOne="Ismigül Kursun" headingTwo="Klinisch Psycholoog"/>

    <Paragraph paragraphText = "Begeleiding in Zaventem"/>
    
    <div class="buttons">
        <Button buttonText="Afspraak maken" href="/afspraak-maken" --margin-bottom=10px/>
        <Button buttonText="Wat doen we?" href="/wat-doen-we" --margin-bottom=10px/>
        <Button buttonText="Meer over Ismigül" href="/meer-over-ismigul" --margin-bottom=10px/>
    </div>
    
    <img class="lottie" src="/psychology-image.png" alt="Psychology"/>
    
</div>
