<script lang="ts">
    import Button from "./Button.svelte";
    import Paragraph from "./Paragraph.svelte";
    import Photo from "./Photo.svelte";
    let { img, firstName, lastName, position,  } = $props()
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

    @media (min-width: 712px) {
        .card {
            width: 350px;
        }
    }
</style>

<div class="card">
    <div style="padding-top: 10px;">
        <Photo {img}/>
    </div>

    <Paragraph 
        paragraphText="{firstName + " " + lastName} <br/> {position}"
        --padding-top=0px
        --padding-bottom=0px
        />

    <div style="padding-block: 32px;">
        <Button buttonText = "meer informatie" href='/teamlid/{firstName}-{lastName}' --background-color="#EDCFB0"/>
    </div>
</div>
