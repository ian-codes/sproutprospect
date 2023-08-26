<script>
    import { isOpen } from "./schedulePopupState";

	let isOpenValue;

    isOpen.subscribe((value) => {
        isOpenValue = value;
    });

    function handleClose() {
        isOpen.update((value) => !value )
    }
</script>

{#if isOpenValue}
    <div class="container">
        <button on:click={handleClose} class="close">Close X</button>
        <div class="bg"></div>
        <iframe class="schedule" title="schedule"
        src="https://calendar.google.com/calendar/appointments/schedules/AcZssZ0Q5HpIOTpG-Jgz1gCRY-5amYSrMNJ0BtXUazusF99N2lD4RAJ-JGKR3vUiBILB9k_i-1H5yHeZ?gv=true"
        style="border: 0" width="100%" height="600" frameborder="0"></iframe>
    </div>
{/if}




<style>
    .container {
        position: fixed;
        inset: 0;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        z-index: 20;
        margin: 1em;
    }

    .close {
        color: white;
        font-size: 1.2em;
        padding: .5em;
        background: rgba(0, 0, 0, 0.452);
        border-radius: 1em;
        border: 2px dotted white;
    }

    .bg {
        inset: 0;
        background: black;
        position: fixed;
        z-index: -1;
        opacity: .7;
        pointer-events: none;
    }

    .schedule {
        background: white;
        padding: 1em;
        margin: 2em;
        border-radius: 1em;
        max-width: 1100px;
        box-shadow: 0 30px 50px black;
    }
</style>