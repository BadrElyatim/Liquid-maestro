<template>
    <div class="hero">
        <header>
            <img class="logo" src="./icons/logo.svg" alt="">
            <img class="hamburger" src="./icons/hamburger-menu.svg" alt="">
        </header>
        <div class="hero__content">
            <p class="indulge">Indulge in</p>
            <h2 class="hero__title">Liquid<br />Artistry</h2>
            <p class="hero__description">Step into a world of<br />extraordinary flavors and<br />unrivaled mixology expertise</p>
            <img class="note" src="./icons/note.svg" alt="">
        </div>

        <button class="explore-btn">EXPLORE</button>

        <img class="curve" draggable="false" src="./icons/line.svg" alt="">
    </div>
</template>

<style scoped>
.hero {
    background-image: url('@/assets/hero.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    padding-bottom: 7em;
    position: relative;
    overflow: hidden;
}

.curve {
    position: absolute;
    right: -10px;
    top: -110px;
}



.hero header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 2em 3em;
}

.hero header .logo {
    height: 80px;
}

.hero .hero__content {
    margin-top: 10em;
    padding-left: 12em;
    padding-bottom: 10em;
    max-width: 1300px;
    margin-inline: auto;
    position: relative;
    float: left;
}

@media (max-width: 800px) {
    .hero .hero__content {
        margin-top: 5em;
        max-width: max-content;
        float: none;
        padding-left: 0;
        padding-top: 0;
        margin-inline: auto;
    }

    .hero .hero__content .hero__title {
        font-size: 5.25rem !important;
    }
}

@media (max-width: 400px) {

    .hero .hero__content .hero__title {
        font-size: 4.25rem !important;
    }
    .hero .hero__content .hero__description {
        font-size: 1.2rem !important;
    }
    .hero .hero__content .note{
        transform: translate(25px, -60%) !important;
        
    }
    .hero header {
        padding: 2em 2em;
    }
}

.hero .hero__content .note{
    position: absolute;
    right: 0;
    top: 0;
    transform: translate(15px, -60%);
}

.hero .hero__content .indulge {
    font-size: 1rem;
    font-family: 'Montserrat', sans-serif;
    font-weight: 400;
    position: relative;
    top: 1px;
}

.hero .hero__content .hero__title {
    font-size: 6.375rem;
    line-height: 104.5%;
}

.hero .hero__content .hero__description {
    line-height: 138.5%;
    font-size: 1.25rem;
    font-weight: 300;
    letter-spacing: .2px;
    margin-top: 1.1em;

}

.hero .explore-btn {
    border: 1px solid #FFF;
    padding: .8em 3.6em;
    margin-inline: auto;
    display: block;
    background-color: transparent;
    color: #FFF;
    font-size: 1rem;
    font-weight: 500;
    transition: .4s all ease;
    clear: left;
}

.hero .explore-btn:hover {
    background-color: #FFF;
    color: #000;
}
</style>