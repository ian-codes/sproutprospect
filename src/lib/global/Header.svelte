<script>
    import { base } from "$app/paths";
    import Incentive from "./Incentive.svelte";

    let isOpen = false

    function handleClick() {
        isOpen = !isOpen
    }
</script>


<header>
    <div class="container">
        <div title="home" style="background-image: url('{base}/logo.png');" 
        class="logo">
        </div>



        <nav>
            <div on:click={handleClick} class="burger">
                <span></span>
                <span></span>
                <span></span>
            </div>

            <ol style="display: {isOpen ? "flex" : "none"}">
                <li>
                    <Incentive />
                </li>
    
                <li>
                    <a href="#">
                        How it Works
                    </a>
                </li>
        
                <li>
                    <a href="#">
                        Our Guarantee
                    </a>
                </li>
        
                <li>
                    <a href="#">
                        Contact Us
                    </a>
                </li>
            </ol>
        </nav>
    </div>
</header>

<style>
    @media screen and (max-width: 950px) {
        .logo {
            margin: .5em 0 !important;
        }


        nav {
            position: relative;
        }

        .burger {
            display: flex !important;
        }

        ol {
            flex-direction: column !important;
            position: absolute;
            top: 4em;
            right: 0;
            background: white;
            padding: .5em;
            z-index: 10;
            width: max-content;
            border-radius: 1em;
            box-shadow: 0 10px 20px black;
        }

        a:hover {
            background: lightgray;
        }

        a::after {
            display: none;
        }
    }


    .burger {
        display: none;
        flex-direction: column;
        justify-content: space-evenly;
        width: 35px;
        height: 35px;
        cursor: pointer;
        transition: all .1s ease;
        padding: .5em;
    }

    .burger:hover {
        box-shadow: 0 0 5px inset black;
    }

    .burger span {
        background: black;
        width: 100%;
        height: 3px;
        border-radius: 5px;
    }

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