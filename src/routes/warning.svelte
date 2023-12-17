<div class="warning">
    <div class="warningText">
        <span class="material-symbols-outlined">warning</span>
        <p>Warning:</p>
    </div>
    <p><slot/></p>
</div>

<style scoped>
    .warning{
        border: 1px solid rgba(253, 137, 42, 0.747);
        border-radius: 10px;
        padding: 10px;
        display: grid;
        grid-template-columns: 100px 1fr;
        gap: 20px;
    }

    .warning .warningText{
        display: flex;
    }

    .warning p{
        color: rgba(253, 137, 42, 0.747);
        display: flex;
        align-items: center;
    }

    .warning span{
        color:rgba(253, 137, 42, 0.747)
    }
</style>