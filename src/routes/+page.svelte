<script>
    import { base } from "$app/paths";
    import Incentive from "../lib/global/Incentive.svelte";

</script>

<section>
    <div style="background-image: url('{base}/bg2.jpg')" class="bg"></div>

    <h1>
        Landscaping Client Acqusition Has Never Been Simpler.
    </h1>
    
    <p>
        We help landscaping businesses optimize & automate their client acquisition using the power of our Digital Sprouting© solution.
    </p>

    <Incentive title="Learn More" />
</section>



<style>
    section {
        position: relative;
    }

    .bg {
        position: fixed;
        inset: 0;
        background-position: center;
        background-repeat: no-repeat;
        background-size: cover;
        filter: brightness(.3) saturate(.5);
        z-index: -2;
        pointer-events: none;
    }

    .bg::after {
        content: '';
        position: absolute;
        inset: 0;
        opacity: .4;
        background: radial-gradient(transparent, rgb(4, 14, 54));
    }


    h1 {
        text-shadow: 0 0 20px rgba(214, 229, 248, 0.3);
        color: white;
        font-size: 3.5em;
        margin-bottom: 2rem;
    }

    p {
        color: white;
        font-size: 2em;
        font-weight: normal;
    }
</style>