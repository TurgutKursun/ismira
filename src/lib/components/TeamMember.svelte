<script lang="ts">
    import Button from "./Button.svelte";
    import Paragraph from "./Paragraph.svelte";
    import Photo from "./Photo.svelte";
    let { img, name, position,  } = $props()
</script>

<style>
    .card {
        background-color: #FF8C00;
        margin-inline: 40px;
        border: 3px solid black;
        border-radius: 16px;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }
</style>

<div class="card">
    <div style="padding-block: 0px;">
        <Photo {img}/>
    </div>

    <Paragraph 
        paragraphText="{name} <br/> {position}"
        --padding-top=0px
        --padding-bottom=0px
        />

    <div style="padding-block: 32px;">
        <Button buttonText = "meer informatie" --background-color="#EDCFB0"/>
    </div>
</div>
