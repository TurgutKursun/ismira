<script lang="ts">
    import Address from "$lib/components/Address.svelte";
    import Button from "$lib/components/Button.svelte";
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
            padding-top: 30px
        }

        .content {
            grid-column: 1; 
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            border-right: 2px solid black;
        }

        .map {
            grid-column: 2; /* Place iframe in the second column */
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            margin-block: 30px
        }

        iframe {
            height: 500px;
        }
    }
</style>

<Heading headingOne="Afspraak maken" headingTwo=""/>

<div class="container">
    <div class="content">
        <Paragraph 
            paragraphText="Om een afspraak te maken, of voor meer informatie, kan u ons altijd </br> bereiken via e-mail, sms, of gsm"
            --padding-top=0
            --padding-bottom=0
            />

        <Icon icon="calendar_month" size=40px padding_bottom="0px" padding_top="60px"/>
        <Paragraph paragraphText="Online afspraak maken binnenkort beschikbaar*" --padding-top=0 --padding-bottom=0/>

        <Icon icon="mail" size=40px padding_top="40px"/>
        <Paragraph paragraphText="We beantwoorden uw vragen zo snel mogelijk, meestal binnen de 24u*" --padding-top=0px --padding-bottom=0px/>
        <Button buttonText="Stuur uw bericht" href="https://www.vind-een-psycholoog.be/psycholoog/ismigul-kursun-zaventem.html" --margin-top=10px --margin-bottom=10px/>

        <Icon icon="phone" size=40px padding_top="40px"/>
        <Paragraph paragraphText="Bereikbaar maandag - vrijdag tussen 09h00 en 16h00*" --padding-top=0px --padding-bottom=0px/>
        <PhoneNumber number="+32495674687" --padding-top=0 --padding-bottom=40px/>

        <Icon icon="euro" size=40px padding_bottom="0px" padding_top="0px"/>
        <Paragraph paragraphText="Een consultatie van ± 45 minuten kost €70,00" --padding-top=0 --padding-bottom=60px/>
        
        <Paragraph paragraphText="*Een afspraak dient minstens 48 uur voor aanvang van de sessie geannuleerd te worden. Bij laattijdige annulatie zijn wij genoodzaakt de volledige sessie in rekening te brengen. Door een sessie te boeken (telefonisch, via e-mail, online of per sms) gaat u akkoord met deze voorwaarden."
            --padding-top=0px --padding-bottom=0px/>
    </div>
    <div class="map">
        <Icon icon="location_on" size=40px/>
        <Address address="Excelsiorlaan 44, 1930 Zaventem" --padding-bottom=0px --padding-top=0px --margin-top=30px --margin-bottom=30px/>

        <iframe 
            title=""
            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2517.2364981005394!2d4.453097976753747!3d50.88233307167785!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x47c3dcfc45287657%3A0xd1e1defd125e5071!2sExcelsiorlaan%2044%2C%201930%20Zaventem!5e0!3m2!1sen!2sbe!4v1755765666731!5m2!1sen!2sbe"

            width="85%" 
            height="300px"
            style="padding-top=0px; border:0; border-radius: 32px; margin-bottom: 30px"  
            loading="lazy" 
            referrerpolicy="no-referrer-when-downgrade">
        </iframe>

        </div>
</div>
