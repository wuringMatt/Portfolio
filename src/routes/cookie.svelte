<script>
    //declare reactive variable
    $: displayCookie = false;

    //function for checking if the cookie already exists
    function checkCookies(){
        let currentCookie = document.cookie.split("=");
        //if the cookie exists don't display the notification, else display it.
        if(currentCookie[0] == "chocolateChipCookie"){
            displayCookie = false;
        } else {
            displayCookie = true;
        }
    }

    //function that sets the cookie
    function addCookie(){
        //get the time 2 minutes from now
        let d = new Date();
        d.setMinutes(2 + d.getMinutes());

        //set the cookie and disable the notification
        document.cookie = `chocolateChipCookie=deliciousCookie; expires = ${d};`;
        displayCookie = false;
    }

</script>

<!-- Hopefully you can respect the cookie puns, if not I'm sorry :) -->

<!-- on load call checkCookies function -->
<svelte:window on:load="{checkCookies()}"/>

<!-- Cookie notification Component -->
<!-- Set the visibility depending on if displayCookie is true or false -->
<div class="cookie" style="visibility:{displayCookie ? "visible" : "hidden"};">
    <!-- styling element -->
    <div class="cookieWrapper"></div>
    <!-- Grid element for all the ingredients that make up a cookie notification -->
    <div class="ingredients">
        <!-- title element / the chocolate chips on top of the cookie -->
        <h2 class="chocolateChips">
            This Website Uses Cookies
        </h2>
        <!-- the cookie dough, the text that makes up most of the notification -->
        <p class="cookieDough">
            Our website uses cookies to provide your browsing experience and relevant information. Before continuing to use our website, you agree & accept of our
            <!-- the secret ingredient that leads to you to the cookie policy -->
            <a class="secretIngredient" href="https://www.cookiepolicygenerator.com/live.php?token=69VOSeblVpoO8U3G1cQas7pjJszmurqu" target="_blank">
                Cookie Policy & Privacy.
            </a>
        </p>
        <!-- when you eat the cookie it will call the addCookie function -->
        <button class="eat" on:click={addCookie}>Accept</button>
    </div>
</div>

<style scoped>
    .cookie{
        position: fixed;
        bottom: 15px;
        right: 15px;
        width: 500px;
        height: 200px;
        background-color: rgb(36, 36, 49);
        visibility: visible;
    }   

    .cookieWrapper{
        position: absolute;
        left: 0;
        height: 100%;
        border: 4px solid darkorange;
    }

    .ingredients{
        display: grid;
        grid-template-columns: 1fr;
        gap: 18px;
        padding: 10px 10px 10px 18px;
        width: 100%;
    }

    h2{
        font-size: 1.4rem;
        font-weight: 500;
    }

    p{
        line-height: 120%;
    }

    p .secretIngredient{
        color: darkorange;
    }

    button{
        width: 150px;
        padding: 10px;
        border: none;
        background-color: darkorange;
        color: white;
        font-size: 1rem;
        border-radius: 10px;
    }
</style>