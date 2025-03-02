<script>
    import Button from "$lib/components/Button.svelte";
    import Heading from "$lib/components/Heading.svelte";
    import Paragraph from "$lib/components/Paragraph.svelte";
    import { DotLottieSvelte } from '@lottiefiles/dotlottie-svelte';    
</script>

<style>
    .lottie {
        margin: 0px;
        padding: 0px;
        margin-top: 30px;
    }
    .buttons {
        display: flex;
        flex-direction: column;
        align-items: center;
    }
</style>

<Heading headingOne="Ismira" headingTwo="Groepspraktijk"/>

<Paragraph paragraphText = "Psychologisch begeleiding <br> in Zaventem"/>

<Paragraph paragraphText = "Iedereen heeft af en toe <br> een luisterend oor nodig"/>

<div class="lottie">
    <DotLottieSvelte
    src="https://lottie.host/d681077d-5d27-45d6-8d34-8c242d6442ff/S3tEmV2oWK.lottie"
    loop
    autoplay
  />
</div>

<div class="buttons">
    <Button buttonText="Afspraak maken" --margin-bottom=20px/>
    <Button buttonText="Wat doen we?" --margin-bottom=20px/>
    <Button buttonText="Wie is wie?"/>
</div>
