<script>
    import Introduction from "./introduction.svelte";
    import Warning from "./warning.svelte";
    import Projects from "./projects.svelte";
    import Cookie from "./cookie.svelte";

    import logo from "$lib/img/Logo.svg";

    import github from "$lib/img/github-mark-white.svg";
    import linkedIn from "$lib/img/linkedin.png";
    import email from "$lib/img/mail.png";
</script>

<Cookie/>

<div class="nav">
    <img src="{logo}" alt="">
    <div class="links">
        <a href="https://github.com/wuringMatt" target="_blank"><img src="{github}" alt="github"></a>
        <a href="https://www.linkedin.com/in/matt-wuring-4533b31b8/" target="_blank"><img src="{linkedIn}" alt="linkedIn"></a>
        <a href="mailto:matt.wuring@gmail.com" target="_blank"><img src="{email}" alt="email"></a>
    </div>
</div>

<section>
    <h1>
        <span>My name is Matt</span><br>
        <span>and I'm a Software Developer.</span>
    </h1>

    <Warning>
        This website is still under construction. Please be aware of this whilst browsing.
    </Warning>

    <Introduction/>

    <Projects/>
</section>

<style scoped>
    .nav{
        position: fixed;
        top: 0;
        left: 0;
        padding: 10px;
        display: grid;
        grid-template-columns: 1fr;
        gap: 15px;
        justify-content: center;
        align-items: center;
    }

    .nav img{
        height: 40px;
    }

    .links{
        display: grid;
        grid-template-rows: 1fr 1fr 1fr;
        gap: 10px;
    }

    .links img, .links a{
        width: 32px;
        height: 32px;
    }

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
</style>