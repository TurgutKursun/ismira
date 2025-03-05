<script lang="ts">
    import Address from "$lib/components/Address.svelte";
import Email from "$lib/components/Email.svelte";
import Heading from "$lib/components/Heading.svelte";
    import Icon from "$lib/components/Icon.svelte";
    import Paragraph from "$lib/components/Paragraph.svelte";
    import PhoneNumber from "$lib/components/PhoneNumber.svelte";
</script>

<style>
    .column {
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    .map {
        max-width: 200px;
        max-height: 200px;
    }
</style>


<div class="column">
    <Heading headingOne="Ismira" headingTwo="Afspraak maken"/>
    <Paragraph paragraphText="Om een afspraak te maken, of voor <br/> meer informatie, kan u ons altijd </br> bereiken via e-mail, sms, of gsm"/>

    <Icon icon="mail" size=40px/>
    <Email email="info@ismira.com" --padding-bottom=20px/>
    <Paragraph paragraphText="We beantwoorden uw mails <br/> zo snel mogelijk, vaak binnen de 24u" --padding-top=0px/>

    <Icon icon="phone" size=40px/>
    <PhoneNumber number="+32494130449" --padding-bottom=20px/>
    <Paragraph paragraphText="Bereikbaar maandag - vrijdag <br/> tussen 09h00 en 16h00" --padding-top=0px/>

    <Icon icon="location_on" size=40px/>
    <Address address="Brussel, Zaventem, Vlinderstraat 28" --padding-bottom=20px/>
    <iframe 
        title=""
        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2512.5574669225693!2d4.5052269772370055!3d50.96888567169585!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x47c3e6df12b7d241%3A0xc166ae1c165cc91a!2sVlinderstraat%2C%201982%20Zemst!5e0!3m2!1sen!2sbe!4v1740938947066!5m2!1sen!2sbe" 
        width="90%" 
        height="300px" 
        style="padding-top=0px; border:0; border-radius: 32px; margin-bottom: 30px"  
        loading="lazy" 
        referrerpolicy="no-referrer-when-downgrade">
    </iframe>
</div>
