<script lang="ts">
    import Button from "./Button.svelte";
    import Heading from "./Heading.svelte";
    import Icon from "./Icon.svelte";
    import Paragraph from "./Paragraph.svelte";
    import Photo from "./Photo.svelte";

    let { name, position, description, photoFileName, university, degree } = $props()
</script>

<style>
    .page {
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    .opleiding {
        display: flex;
        align-items: center;
        gap: 10px;
    }
</style>

<div class="page">
    <div>
        <Heading headingOne={name} headingTwo={position} />
    </div>

    <div style="margin-top: 0px; margin-bottom: 0px;"> 
        <Photo img={photoFileName}/>
    </div>

    <Paragraph paragraphText={description} --max-width=1300px --padding-inline=25px --text-align="justify" --padding-top=0px --padding-bottom=20px/>
    
    <div class="opleiding">
        <h2 style="margin-block: 0px;">Opleiding</h2>
        <Icon icon="school"/>
    </div>
    
    <Paragraph paragraphText="{university} <br/> {degree}" --padding-top=10px --padding-bottom=30px/>
    
    <Button buttonText="afspraak maken" href='/afspraak-maken'/>
</div>
