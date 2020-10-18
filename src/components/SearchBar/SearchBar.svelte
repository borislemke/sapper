<script>
    let showPanel = false

    const listOfArea = [
        "Canggu",
        "Seminyak",
        "Ubud",
        "Legian",
        "Umalas"
    ]

    const setPanelState = (state) => () => showPanel = state
</script>

<style>
    .wrapper {
        padding: 12px 24px;
        position: relative;
    }

    label {
        background-color: white;
        border-radius: var(--radius);
        display: flex;
        height: 52px;
        padding: 0 16px;
    }

    input {
        background-color: transparent;
        border: 0;
        margin: 0;
        outline: none;
        padding: 0;
        width: 100%;
    }

    ::-webkit-input-placeholder {
        text-align: center;
    }

    :-moz-placeholder { /* Firefox 18- */
        text-align: center;
    }

    ::-moz-placeholder { /* Firefox 19+ */
        text-align: center;
    }

    :-ms-input-placeholder {
        text-align: center;
    }

    .panel {
        background-color: white;
        border-radius: var(--radius);
        display: none;
        padding: 16px;
    }

    .panel.active {
        display: block;
    }

    .search-item {
        align-items: center;
        display: flex;
        height: 40px;
    }
</style>

<div
        class="wrapper"
        style="--radius: 4px;">
    <label>
        <input
                id="search"
                type="text"
                autocomplete="off"
                on:focus={setPanelState(true)}
                placeholder="Where are you going?">
    </label>
    <div
            class="panel"
            class:active={showPanel}
            on:focus={setPanelState(false)}>
        {#each listOfArea as area}
            <div class="search-item">
                {area}
            </div>
        {/each}
    </div>
</div>
