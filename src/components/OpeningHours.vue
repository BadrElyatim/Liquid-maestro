<template>
    <div class="opening-hours">
        <h4>Opening <span>Hours</span></h4>
        <div class="hours">
            <p>Mon - Thu: <span class="hour">5 PM - 12 AM</span></p>
            <p>Fri - Sat: <span class="hour">5 PM - 2 AM</span></p>
            <p>Sun: Closed</p>
        </div>
    </div>
</template>

<style scoped>
    .opening-hours {
        padding: 5em 28em 5em 8em;
        max-width: 1300px;
        margin-inline: auto;
    }
    @media (max-width: 1000px) {
        .opening-hours {
            padding: 5em 21em 5em 4em;
        }

    }

    @media (max-width: 600px) {
        .opening-hours {
            padding: 5em 2em;
        }
    }

    .opening-hours h4 {
        color: #D16868;
        font-size: 2.25rem;
        font-weight: 500;
    }

    @media (max-width: 1000px) {
        .opening-hours h4 {
            font-size: 2rem;
        }
    }
    .opening-hours h4 span {
        font-weight: 300;
    }

    .opening-hours .hours {
        margin-top: 2.3em;
    }

    .opening-hours .hours p {
        padding-top: .4em;
        padding-bottom: .4em;
    }

    @media (max-width: 1000px) {
        .opening-hours .hours p {
            font-size: 1.37rem !important;
        }
    }

    .opening-hours .hours p {
        background-image: linear-gradient(to right, #333 70%, rgba(255, 255, 255, 0) 10%);
        background-position: top;
        background-size: 6px 1px;
        background-repeat: repeat-x;
        position: relative;
        font-size: 1.5rem;
        font-family: 'Montserrat', sans-serif;
        font-weight: 200;
    }   

    .opening-hours .hours p:last-child::before {
        content: '';
        width: 100%;
        display: block;
        position: absolute;
        height: 1px;
        top: 0;
        background-image: linear-gradient(to right, #333 70%, rgba(255, 255, 255, 0) 10%);
        background-position: bottom;
        background-size: 6px 1px;
        background-repeat: repeat-x;
    }
    .opening-hours .hours p:last-child {
        background-image: linear-gradient(to right, #333 70%, rgba(255, 255, 255, 0) 10%);
        background-position: bottom;
        background-size: 6px 1px;
        background-repeat: repeat-x;
        
    }

    .opening-hours .hours .hour {
        font-weight: 400;
    }
</style>