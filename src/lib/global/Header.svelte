<script>
    import { base } from "$app/paths";
    import Incentive from "./Incentive.svelte";
</script>


<header>
    <div class="container">
        <div title="home" style="background-image: url('{base}/logo.png');" 
        class="logo">
        </div>

        <nav>
            <ol>
                <li>
                    <Incentive />
                </li>
    
                <li>
                    <a href="how-it-works">
                        How it Works
                    </a>
                </li>
        
                <li>
                    <a href="guarantee">
                        Our Guarantee
                    </a>
                </li>
        
                <li>
                    <a href="contact">
                        Contact Us
                    </a>
                </li>
            </ol>
        </nav>
    </div>
</header>

<style>
    header {
        background: white;
        padding: 0 1em;
        margin-bottom: 2em;
        box-shadow: 0 5px 20px rgba(255, 255, 255, 0.164);
    }

    .container {
        max-width: 1200px;
        margin: 0 auto;
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
    }

    .logo {
        background-repeat: no-repeat;
        background-size: contain;
        background-position: center;
        width: 120px;
        height: 120px;
        margin: 1em;
        cursor: pointer;
    }

    .logo:hover {
        box-shadow: 0 0 0 1px black;
    }

    ol {
        display: flex;
        flex-direction: row;
        gap: 2em;
    }

    a {
        position: relative;
        display: block;
        font-weight: bold;
        letter-spacing: 1px;
        padding: 1em;
        border-radius: 1em;
        transition: all .1s ease;
        user-select: none;
    }

    a::after {
        position: absolute;
        content: '';
        bottom: 0;
        left: 1em;
        height: 2px;
        width: 0;
        background: black;
        border-radius: 1em;
        transition: all .3s ease;
    }

    a:hover::after {
        width: calc(100% - 2em);
    }
</style>