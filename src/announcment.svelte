<script>
    let show = true;

    const hideAlert = () => {
        show = false;
    }
    const showAlert = () => {
        show = true;
    }
    let warning = true;
</script>

<!-- {#if show === true}
    <div class="alert" class:warning={warning}>
        FRUIT SHOP
        <button on:click={hideAlert}>X</button>
    </div>
{/if} -->

{#if show === true}
{#if warning === true}
    <div class="alert" class:warning>
        FRUIT SHOP
        <button on:click={hideAlert}>X</button>
    </div>
{/if}
{/if}
{#if show === false}
    <button on:click={showAlert}>+</button>
{/if}


<style>
    
    .alert {
        margin-top: 10px;
        padding: 8px;
        font-size: 18px;
        background-color: darkseagreen;
        color: darkslategray;
    }
    .warning {
        background-color: red;
    }
</style>