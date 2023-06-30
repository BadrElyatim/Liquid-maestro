<script setup>
    import Calendar from './Calendar.vue';
</script>

<template>
    <div class="contact">
        <img class="B" src="./icons/B.svg" alt="">
        <div class="wrapper">
            <h4>Bookings <span>& Contact</span></h4>
            <form @submit.prevent="" action="" class="contact__form">
                <div class="input-field">
                    <label for="">Name</label>
                    <input type="text" placeholder="Name">
                </div>
                <div class="input-field">
                    <label for="">Email</label>
                    <input type="text" placeholder="Email">
                </div>
                <div class="input-field">
                    <label for="">Phone</label>
                    <input type="text" placeholder="Phone">
                </div>
                <div class="input-field">
                    <label for="">Number of people</label>
                    <input type="text" placeholder="Number of people">
                </div>

                <Calendar />
                <button class="submit" type="submit">SUBMIT</button>
                <div class="contact__info">
                    <h5>Contact info</h5>
                    <div class="info">
                        <label for="">Phone</label>
                        <p>(555) 123-4567</p>
                    </div>
                    <div class="info">
                        <label for="">Email</label>
                        <p class="email">info@liquidmaestro.com</p>
                    </div>
                </div>
            </form>
        </div>
    </div>
</template>

<style scoped>
    .contact {
        display: flex;
        justify-content: space-between;
        gap: 100px;

    }

    @media (max-width: 1000px) {
        .contact {
            padding: 5em 0 5em 0;
            overflow: hidden;
        }
        .contact .B {
            height: 700px;
        }

        .contact > .wrapper {
            padding-right: 10em;
        }

    }

    @media (max-width: 800px) {
        .contact {
            flex-direction: column;
            gap: 50px;
        }

        .contact .B {
            height: 600px;
            transform: translateX(-25%);
        }

        .contact > div.wrapper {
            padding-left: 4em !important;
        }
    }

    @media (max-width: 600px) {
        .contact {
            padding: 5em 2em !important;
        }
        .contact > div.wrapper {
            padding: 0 !important;
            margin-right: 0 !important;
        }


    }



    .contact > .wrapper {
        flex: 1;
        padding: 3em 0em;
        margin-right: 5em;
    }
    .contact h4 {
        color: #D16868;
        font-size: 2.25rem;
        font-weight: 500;
        margin-bottom: 1.7em;
    }

    .contact__form .input-field {
        margin-bottom: 2.1em;
    }

    .contact__form label{
        display: block;
        font-size: .75rem;
        font-family: 'montserrat', sans-serif;
    }

    .contact__form input {
        width: 100%;
        border: none;
        outline: none;
        background-color: #181818;
        font-size: 1.312rem;
        font-family: 'montserrat', sans-serif;
        margin-top: 6px;
        border-bottom: 1px solid #6F6F6F;
        color: #FFF;
    }

    .submit {
        margin-top: 2.5em;
        background-color: transparent;
        border: 1px solid #FFF;
        color: #FFF;
        padding: .8em 3.8em;
        font-size: 1rem;
        transition: .4s all ease;
        font-weight: 600;
        cursor: pointer;
    }

    .submit:hover {
        color: #000;
        background-color: #FFF;
    }

    .contact__info {
        margin-top: 5em;
    }

    .contact__info h5 {
        font-size: 1.75rem;
        color: #D68F78;
    }

    .contact__info .info {
        margin-top: 1em;
    }

    .contact__info .info .email {
        text-decoration: underline;
        text-underline-offset: 2px;
    }

    .contact__info .info p {
        margin-top: .3em;
        font-size: 1.25rem;
        font-family: 'montserrat', sans-serif;
        font-weight: 300;
    }
</style>