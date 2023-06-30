<template>
    <div class="wrapper">
        <div class="intro">
            <img class="bar-spoon" src="./icons/bar-spoon.svg" alt="">
            <img class="charlotte" src="@/assets/pexels-charlotte-may.jpg" alt="">
            <p class="first-description">Liquid Maestro, the newest hotspot in downtown Los Angeles. Our skilled mixologists are passionate about crafting exceptional cocktails that will delight your senses.</p>
            <p class="second-description">With an ambiance that exudes elegance and a commitment to delivering unforgettable experiences, Liquid Maestro is the ultimate destination for cocktail enthusiasts. Join us for an exquisite journey into the world of liquid artistry.</p>
            <img class="A" src="./icons/A.svg" alt="">
        </div>
    </div>
</template>


<style scoped>
    .wrapper {
        transform: scale(1);
    }
    .intro {
        padding: 5em 14em;
        max-width: 1300px;
        margin-inline: auto;
        position: relative;
        overflow: hidden;
    }

    .bar-spoon {
        position: fixed;
        top: 0;
        left: 50%;
        z-index: 100;
        transform: translate(-50%, -50%);
    }

    .intro .charlotte {
        margin: auto;
        display: block;
    }

    .intro .first-description {
        font-size: 2.25rem;
        line-height: 138.5%;
        font-weight: 300;
        transform: translateY(-50%);
    }

    .intro .second-description {
        position: relative;
        bottom: 45px;
        font-size: 1.125rem;
        font-family: 'montserrat', sans-serif;
        font-weight: 300;
        line-height: 150%;
        background-color: #181818;
        z-index: 10;
    }

    .intro .A {
        position: absolute;
        top: 0;
        left: 0;
    }

    @media (max-width: 1000px) {
        .intro {
            padding: 5em 7em;
        }

        .intro .first-description {
            font-size: 1.75rem;
        }
    }

    @media (max-width: 700px) {
        .intro {
            padding: 5em 2em;
        }

        .intro .first-description {
            font-size: 1.5rem;
        }

        .intro .second-description {
            bottom: 10px;
        }
    }


</style>