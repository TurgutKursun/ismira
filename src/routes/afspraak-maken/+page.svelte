<script lang="ts">
    import Address from "$lib/components/Address.svelte";
import Email from "$lib/components/Email.svelte";
import Heading from "$lib/components/Heading.svelte";
    import Paragraph from "$lib/components/Paragraph.svelte";
    import PhoneNumber from "$lib/components/PhoneNumber.svelte";
</script>

<style>
    .column {
        display: flex;
        flex-direction: column;
        align-items: center;
    }
</style>


<div class="column">
    <Heading headingOne="Ismira" headingTwo="Afspraak maken"/>
    <Paragraph paragraphText="Om een afspraak te maken, of voor <br/> meer informatie, kan u ons altijd </br> bereiken via e-mail, sms, of gsm"/>

    <span class="material-icons-outlined" style="font-size: 36px;">mail</span>
    <Email email="info@ismira.com" --padding-bottom=20px/>
    <Paragraph paragraphText="We beantwoorden uw mails <br/> zo snel mogelijk, vaak binnen de 24u" --padding-top=0px/>

    <span class="material-icons-outlined" style="font-size: 36px;">phone</span>
    <PhoneNumber number="+32494130449" --padding-bottom=20px/>
    <Paragraph paragraphText="Bereikbaar maandag - vrijdag <br/> tussen 09h00 en 16h00" --padding-top=0px/>

    <span class="material-icons-outlined" style="font-size: 36px;">location_on</span>
    <Address address="Brussel, Zaventem, Vlinderstraat 28" --padding-bottom=20px/>
</div>
