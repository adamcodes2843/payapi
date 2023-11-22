<script>
    let email = "";
    let demoScheduled = false;
    function scheduleDemo() {

    }
</script>

<div>
    <input 
        type="text" 
        bind:value={email}
        placeholder="Enter email address"
    >
    <button type="button" on:click={() => demoScheduled = true} class="schedule-button">Schedule a Demo</button>
</div>

<style>
    div {
        display: flex;
        flex-direction: column;
        gap: 12px;
    }
    input {
        
        font-family: 'Public Sans', sans-serif;
        font-weight: 700;
        color: var(--sanJuanBlue);
        border-radius: 20px;
        border: none;
        padding: 14px 20px;
        font-size: 15px;
        box-shadow: 2px 2px 8px var(--sanJuanBlue);
    }
    input:focus {
        outline: none;
    }
</style>