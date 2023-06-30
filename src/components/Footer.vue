<template>
    <footer>
        <div class="social-media">
            <img src="./icons/instagram.svg" alt="">
            <img src="./icons/twitter.svg" alt="">
            <img src="./icons/facebook.svg" alt="">
        </div>
        <div class="content">
            <img class="logo" src="./icons/logo.svg" alt="">
            <p>World of extraordinary flavors &<br />unrivaled mixology expertise</p>
        </div>
        <div class="copyright">
            <p>Copyright © 2023 XIDE</p>
            <p>Design by <span>XIDE</span></p>
        </div>
    </footer>
</template>

<style scoped>
    footer {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        padding: 2.4em 3.4em;
        background-image: url('@/assets/mask-group.jpg');
        background-repeat: no-repeat;
        background-position: center;
        background-size: cover;
    }

    footer .social-media {
        align-self: flex-end;
    }

    footer .social-media img:nth-child(2) {
        margin-inline: 10px;
    }
    footer .content {
        text-align: center;
        margin-top: 1.7em;
        margin-bottom: 2em;
    }

    footer .content p {
        font-size: 0.687rem;
        font-family: 'Montserrat', sans-serif;
        margin-top: 1em;
    }

    footer .copyright {
        width: 100%;
        display: flex;
        justify-content: space-between;
    }

    footer .copyright p{
        font-family: 'Montserrat', sans-serif;
        font-size: .875rem;
    }

    footer .copyright p span {
        font-family: inherit;
        font-weight: 600;
        text-decoration: underline;
    }

    @media (max-width: 700px) {
        footer {
            padding: 1.3em 2em;

        }

        footer .social-media {
            align-self: auto;
        }

        footer .copyright {
            flex-direction: column;
            align-items: center;
        }

        footer .copyright p:first-child{
            margin-bottom: .3em;
        }
    }
</style>