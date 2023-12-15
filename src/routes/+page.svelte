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

    <div class="introduction">
        <h2>About me</h2>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Eius tenetur quam eos aspernatur vel nisi quaerat dicta, aliquam omnis. Perspiciatis accusamus tempora vitae natus doloremque tenetur commodi explicabo atque blanditiis quaerat deserunt ab aspernatur perferendis adipisci sit, vel earum error eaque repudiandae harum a ad? Ab voluptatibus cum consequatur quos nobis autem, expedita sapiente neque voluptates molestias ad illo commodi, quia esse animi sed. Labore exercitationem vel iste optio veritatis debitis, dicta atque necessitatibus quis perspiciatis modi quasi repudiandae commodi, possimus eligendi maiores adipisci? Doloribus consequatur culpa repellendus iste, voluptatibus voluptatem animi aliquam similique a exercitationem non illo eum ex?</p>
    </div>
</section>

<style scoped>
    section{
        width: 100%;
        padding: 100px 25% 0 25%;
        display: grid;
        grid-template-columns: 1fr;
        gap: 40px;
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

    .introduction h2{
        font-size: 1.5rem;
        font-weight: 600;
        background-color: rgb(36, 36, 49);
        padding: 10px;
        padding-left: 15px;
    }
    
    .introduction p{
        line-height: 150%;
        border: 1px solid rgb(36, 36, 49);
        padding: 10px 15px 10px 15px;
        border-radius: 0 0 15px 15px;
    }
</style>