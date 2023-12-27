<script>
    let email = "";
    let demoScheduled = false;
    let demoWarning = false;
    function enterKey(e) {
        if (e.key === 'Enter') {
            demoScheduled = true;
        }
    }
    let emailCheck = /^\S+@\S+\.\S+$/
    let scheduleDemoClick = () => {
        if (emailCheck.test(email)) {
            demoScheduled = true;
            demoWarning = false;
        } else {
            demoWarning = true;
        }
    }
</script>

<div style="position:relative">
    {#if demoScheduled == false}
    <input 
        type="text" 
        bind:value={email}
        placeholder="Enter email address"
        on:keypress={(e) => enterKey(e)}
    >
    <button disabled={demoScheduled} type="button" on:click={() => scheduleDemoClick()} class="schedule-button">Schedule a Demo</button>
    {:else}
    <p>An email has been sent to {email}!</p>
    {/if}
    {#if emailCheck.test(email) == false && demoWarning}
    <p style="position:absolute; top:-30px; left: 15px; font-weight: 700; color: red; font-size: 14px;">Please enter a valid email</p>
    {/if}
</div>

<style>
    div {
        display: flex;
        flex-direction: column;
        gap: 12px;
    }
    input {
        height: 48px;
        font-family: 'Public Sans', sans-serif;
        font-weight: 700;
        color: var(--sanJuanBlue);
        border-radius: 60px;
        border: none;
        padding-left: 20px;
        padding-right: 20px;
        font-size: 15px;
        box-shadow: 2px 2px 8px var(--sanJuanBlue);
    }
    input:focus {
        outline: none;
    }
    input:hover {
        cursor: pointer;
    }
    @media screen and (min-width: 768px) {
        input {
            max-width: 445px;
        }
        div {
            position: relative;
            max-width: 445px;
            margin: auto;
        }
        button {
            position: absolute;
            right: 0;
        }
    }
    @media screen and (min-width: 1440px) {
        div {
            margin: 0;
            width: 445px;
        }
    }
</style>