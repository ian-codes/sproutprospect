<script>
    export let title = "Book a Free Call"
    export let link

    import { isOpen } from "../schedule/schedulePopupState";


    function handleClick() {
        isOpen.update((value) =>  !value)
    }
</script>


<button on:click={handleClick}>
    <a href="{link}">
        {title}
    </a>
</button>


<style>
    button {
        letter-spacing: 1px;
        font-weight: bold;
        padding: 1em;
        border-radius: .5em;
        color: white;
        margin-right: 1em;
        background: linear-gradient(90deg, rgb(20, 208, 241), rgb(81, 56, 194));
        box-shadow: -1px -1px 2px white, 1px 1px 2px black, 0 4px 10px rgba(0, 0, 0, 0.411);
        transition: all .2s ease;
    }

    button:hover {
        background: linear-gradient(180deg, rgb(20, 208, 241), rgb(81, 56, 194));
        transform: scale(1.05);
        box-shadow: -1px -1px 2px white, 1px 1px 2px black, 0 4px 50px rgba(0, 0, 0, 0.329);
    }

    a {
        color: white;
    }
</style>