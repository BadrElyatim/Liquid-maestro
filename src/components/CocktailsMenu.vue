<script setup>
    import CocktailItem from './CocktailItem.vue';
    import { ref } from 'vue';

    let firstElement = ref(null)
    let secondElement = ref(null)

    let isNormal = true
    const scroll = () => {
        if (isNormal)
            scrollRight()
        else
            scrollLeft()
    }

    const scrollRight = () => {
        firstElement.value.$el.style.right = '100%'
        secondElement.value.$el.style.left = '0'
        secondElement.value.$el.style.transform = 'translateX(0)'
        isNormal = false
    }
    const scrollLeft = () => {
        firstElement.value.$el.style.right = '0'
        secondElement.value.$el.style.left = '100%'
        secondElement.value.$el.style.transform = 'translateX(-25%)'
        isNormal = true
    }
</script>

<template>
    <div class="cocktails-menu">
        <h4>Cocktails <span>Menu</span></h4>
        <div class="caroussel-wrapper">
            <CocktailItem
                ref="firstElement" 
                class="first-item"
                image="image-3.svg"
                indulgent="Indulgent harmony"
                bold-name="Symphony"
                regular-name="in Gold"
                ingredients="Aged bourbon, honey, ginger. "
                description="Experience the symphony of flavors as aged bourbon blends seamlessly with the sweetness of honey & the subtle spice of ginger."
            />
            <img @click="scroll" class="arrow" src="./icons/Circle Arrow.svg" alt="">
            <CocktailItem
                ref="secondElement"
                class="second-item"
                image="image-8.svg"
                bold-name="Enchanted"
                regular-name="Elixir"
                ingredients="Berries, vodka, elderflower."
                description="Let the enchantment unfold as you savor the magical blend of muddled berries, premium vodka, and a hint of elderflower liqueur."    
            />
        </div>
        <img class="vector" src="./icons/vector-1.svg" alt="">
    </div>
</template>

<style>
    .cocktails-menu {
        padding: 5em 0 5em 8em;
        max-width: 1300px;
        margin-inline: auto;
        position: relative;
    }
    @media (max-width: 1000px) {
        .cocktails-menu {
            padding: 5em 0 5em 4em;
        }

        .cocktails-menu .caroussel-wrapper {
            margin-left: 0;
        }

    }

        
    

    @media (max-width: 600px) {
        .cocktails-menu {
            padding: 5em 0 5em 2em;
            padding-top: 1.5em;
        }
    }

    .cocktails-menu h4 {
        color: #D16868;
        font-size: 2.25rem;
        font-weight: 500;
    }

    @media (max-width: 1000px) {
        .cocktails-menu h4 {
            font-size: 2rem;
        }
    }
    .cocktails-menu h4 span {
        font-weight: 300;
    }

    .caroussel-wrapper {
        margin-left: 25%;
        position: relative;
        overflow-x: hidden;
        display: flex;
        align-items: center;
    }

    .caroussel-wrapper .arrow {
        position: absolute;
        right: 15%;
        bottom: 55%;
        z-index: 10;
    }

    .caroussel-wrapper .first-item {
        right: 0;
    }

    .caroussel-wrapper .second-item {
        position: absolute;
        left: 100%;
        transform: translateX(-25%);
        top: 0;
    }

    .cocktails-menu .vector {
        position: absolute;
        top: 100%;
        left: 0;
        width: 100%;
        transform: translateY(-50%);
    }
</style>