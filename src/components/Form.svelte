<script>
    let name = "";
    let email = "";
    let companyName = "";
    let title = "";
    let message = "";
    let yes = false;
    function handleSubmit() {

    }
</script>

<form on:submit={handleSubmit}>
    <input bind:value={name} placeholder="Name"/>
    <input bind:value={email} placeholder="Email Address"/>
    <input bind:value={companyName} placeholder="Company Name">
    <input bind:value={title} placeholder="Title">
    <textarea bind:value={message} placeholder="Message" />
    <div class="opt-in">
        <input type="checkbox" bind:checked={yes} name="checkbox" id="checkbox">
        <label for="checkbox">Stay up-to-date with company announcements and updates to our API</label>
    </div>
    <button class="submit-button" type="submit">Submit</button>
</form>

<style>
    .submit-button {
        font-weight: 700;
        border: 1px solid var(--sanJuanBlue);
        padding: 1rem 1.5rem;
        border-radius: 40px;
        width: 152px;
        background-color: transparent;
    }
    .submit-button:hover {
        background-color: var(--sanJuanBlue);
        color: var(--linkWaterWhite);
        cursor: pointer;
    }
    form {
        display: flex;
        flex-direction: column;
        padding: 0 2.5rem;
        gap: 6px;
        margin-bottom: 5rem;
    }
    input {
        height: 42px;
        max-width: 445px;
        background-color: transparent;
        padding-left: 1rem;
        padding-right: 1rem;
        border: 0;
        border-bottom: 1px solid rgba(54, 83, 107, 0.2);
        opacity: 70%;
        font-size: 15px;
        line-height: 25px;
        font-weight: 400;
        cursor: pointer;
    }
    input:focus {
        opacity: 100%;
        outline: none;
    }
    input:hover {
        opacity: 100%;
    }
    .opt-in {
        display: flex;
        align-items: center;
        gap: 0.5rem;
        margin: 1rem 0;
    }
    #checkbox {
        width: 24px;
        height: 24px;
        background-color: hsl(36536B);
    }
    label {
        cursor: pointer;
    }
    textarea {
        font-family: 'Public Sans', sans-serif;
        font-size: 15px;
        line-height: 25px;
        font-weight: 400;
        height: 89px;
        background-color: transparent;
        padding-left: 1rem;
        padding-right: 1rem;
        padding-top: 1rem;
        border: 0;
        border-bottom: 1px solid rgba(54, 83, 107, 0.2);
        opacity: 70%;
        resize: none;
        cursor: pointer;
    }
    textarea:focus {
        outline: none;
        opacity: 100%;
    }
</style>