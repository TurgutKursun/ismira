<script lang="ts">
    let { headingOne, headingTwo } = $props()
</script>

<style>
    h1 {
        font-family: 'Playfair Display';
        font-size: 24px;
        margin: 0px;
        padding: 0px;
        padding-top: 20px;
        font-weight: normal;
    }
    h2 {
        font-size: 20px;
        margin: 0px;
        padding: 0px;
        font-weight: normal;
    }
    div {
        font-family: 'Playfair Display';
        display: flex;
        flex-direction: column;
        align-items: center;
    }
</style>

<div class="name">
    <h1>
        {headingOne}
    </h1>
    <h2>
        {headingTwo}
    </h2>
</div>

