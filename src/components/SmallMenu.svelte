<script>
    let showMenu = false;
    function menu() {
        showMenu = !showMenu;
    }
</script>

<button type='button' on:click={menu}>
    <img src='../../assets/shared/mobile/menu.svg' alt="menu" class="menu"/>
</button>

{#if showMenu}
    <div class="side-bar">
        <button type="button" on:click={menu}> 
            <img src='../../assets/shared/mobile/close.svg' alt='close menu' class='close' />
        </button>
        <ul class="side-bar-list">
            <li class='menu-link'>
                <a href="/pricing">Pricing</a>
            </li>
            <li class='menu-link'>
                <a href="/about">About</a>
            </li>
            <li class='menu-link'>
                <a href="/contact">Contact</a>
            </li>
            <li class="schedule-button">
                <a href="/contact">Schedule a Demo</a>
            </li>
        </ul>
    </div>
{/if}

<style>
    .side-bar {
        background-color: rgba(27, 38, 47, 0.99);
        position: fixed;
        width: 65%;
        height: 100vh;
        top: 0;
        right: 0;
        color: var(--linkWaterWhite);
        padding: 2.2rem 1.5rem;
        text-align: right;
        z-index: 50;
    }
    .side-bar-list {
        margin-top: 1.5rem;
        display: flex;
        flex-direction: column;
        list-style-type: none;
        border-top: 1px solid rgba(251, 252, 254, 0.2);
        align-items: center;
        gap: 2rem;
        padding: 2.5rem 0;
        font-size: 20px;
        font-weight: 700;
    }
    .menu-link {
        opacity: 70%;
    }
    a {
        color: var(--linkWaterWhite)
    }
    button {
        border: none;
        background: none;
    }
    button:hover {
        cursor: pointer;
    }
    .menu {
        height: 17px;
        width: 28px;
    }
</style>