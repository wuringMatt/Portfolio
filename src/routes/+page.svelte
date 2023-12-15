<script>

</script>

<section> 
    <h1>
        <span>My name is Matt</span><br>
        <span>and I'm a Software Developer.</span>
    </h1>
    <div class="warning">
        <div class="warningText">
            <span class="material-symbols-outlined">warning</span>
            <p>Warning:</p>
        </div>
        <p>This website is still under construction. Please be aware of this whilst browsing.</p>
    </div>
</section>

<style scoped>
    section{
        width: 100%;
        padding: 100px 25% 0 25%;
        display: grid;
        grid-template-columns: 1fr;
        gap: 25px;
    }

    h1{
        font-size: 3.8rem;
        font-weight: 600;
    }

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