<script lang="ts">
    import Address from "$lib/components/Address.svelte";
    import Email from "$lib/components/Email.svelte";
    import Heading from "$lib/components/Heading.svelte";
    import Icon from "$lib/components/Icon.svelte";
    import Paragraph from "$lib/components/Paragraph.svelte";
    import PhoneNumber from "$lib/components/PhoneNumber.svelte";
</script>

<style>
    .container {
        display: grid;
        align-items: center;
        justify-content: center;
        grid-template-columns: 1fr; /* Single column layout for mobile */
        gap: 20px; /* Adds space between grid items */
    }

    .content {
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    .map {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }

    @media (min-width: 768px) {
        .container {
            display: grid;
            align-items:baseline;
            grid-template-columns: 1fr 1fr; 
        }

        .content {
            grid-column: 1; 
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }

        .map {
            grid-column: 2; /* Place iframe in the second column */
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            border-left: 2px solid black;
            margin-block: 30px
        }

        iframe {
            height: 500px;
        }
    }
</style>

<Heading headingOne="Ismira" headingTwo="Contact"/>

<div class="container">
    <div class="content">
        <Paragraph paragraphText="Voor meer informatie kan u ons altijd bereiken via e-mail, sms, of gsm" --padding-top=0px/>

        <Icon icon="mail" size=40px/>
        <Email email="info@ismira.com" --padding-bottom=20px/>
        <Paragraph paragraphText="We beantwoorden uw mails zo snel mogelijk, vaak binnen de 24u" --padding-top=0px/>

        <Icon icon="phone" size=40px/>
        <PhoneNumber number="+32494130449" --padding-bottom=20px/>
        <Paragraph paragraphText="Bereikbaar maandag - vrijdag tussen 09h00 en 16h00" --padding-top=0px/>
    </div>
    <div class="map">
        <Icon icon="location_on" size=40px/>
        <Address address="Brussel, Zaventem, Vlinderstraat 28" --padding-bottom=0px --padding-top=0px --margin-top=30px --margin-bottom=30px/>

        <iframe 
            title=""
            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2512.5574669225693!2d4.5052269772370055!3d50.96888567169585!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x47c3e6df12b7d241%3A0xc166ae1c165cc91a!2sVlinderstraat%2C%201982%20Zemst!5e0!3m2!1sen!2sbe!4v1740938947066!5m2!1sen!2sbe" 
            width="85%" 
            height="300px"
            style="padding-top=0px; border:0; border-radius: 32px; margin-bottom: 30px"  
            loading="lazy" 
            referrerpolicy="no-referrer-when-downgrade">
        </iframe>
    </div>
</div>
