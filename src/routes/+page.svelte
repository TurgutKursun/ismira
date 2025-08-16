<script>
    import Button from "$lib/components/Button.svelte";
    import Heading from "$lib/components/Heading.svelte";
    import Paragraph from "$lib/components/Paragraph.svelte";
</script>

<style>
    .lottie {
        padding: 0px;
        margin-top: 30px;
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
            width: 500px;
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
    <Heading headingOne="Ismira" headingTwo="Groepspraktijk"/>

    <Paragraph paragraphText = "Psychologisch begeleiding <br> in Zaventem"/>
    
    <Paragraph paragraphText = "Iedereen heeft af en toe <br> een luisterend oor nodig"/>
    
    <div class="buttons">
        <Button buttonText="Afspraak maken" href="/afspraak-maken" --margin-bottom=20px/>
        <Button buttonText="Wat doen we?" href="/wat-doen-we" --margin-bottom=20px/>
        <Button buttonText="Wie is wie?" href="/wie-is-wie" --margin-bottom=20px/>
    </div>
</div>
