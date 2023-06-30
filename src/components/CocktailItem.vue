<script setup>
    const props = defineProps(['image', 'indulgent', 'boldName', 'regularName', 'ingredients', 'description'])
    const image = '/src/assets/image3.svg'
</script>

<template>
    <div class="item">
        <img class="item__photo" :src="image" alt="">
        <div class="item__info">
            <div class="item__name">
                <p v-if="props.indulgent" class="indulgent">{{ props.indulgent }}</p>
                <h5>{{ props.boldName }}<br /> <span>{{ regularName }}</span></h5>
            </div>
            <div class="item__description">
                <h6 class="ingredients">{{ props.ingredients }}</h6>
                <p>{{ props.description }}</p>
            </div>
        </div>

    </div>
</template>

<style scoped>
.item {
    position: relative;
    margin-top: 4em;
    display: flex;
    align-items: center;
    transition: all 2s ease;
}

.item__info {
    display: flex;
    gap: 10px;
    transform: translate(-42%, 20%);
    left: 13%;
}

.item__info .item__name {
    position: relative;
}

.item__info .item__name .indulgent {
    white-space: nowrap;
    font-size: .875rem;
    font-weight: 400;
    font-family: 'montserrat', sans-serif;
    position: absolute;
    top: -15px;
}

.item__info .item__name h5 {
    font-size: 2.625rem;
    font-weight: 600;
    line-height: 120%;
    margin-top: .1em;
}

.item__info .item__name h5 span {
    font-weight: 300;
}

.item__description {
    font-family: 'montserrat', sans-serif;
    letter-spacing: .6px;
    line-height: 356%;
    margin-left: .4em;

}

.item__description .ingredients {
    font-size: .75rem;
    white-space: nowrap;
    font-weight: 500;
}

.item__description p {
    font-weight: 100;
    line-height: 20px;
    position: relative;
    top: -17px;
    font-size: .9rem;
    width: 250px;
}

@media (max-width: 800px) {

    .item .item__photo {
        height: 260px;
    }

    .item__info {
        flex-direction: column;
        transform: translate(-70%, 25%);
    }

    .item__description {
        line-height: normal;
    }

    .item__description p {
        margin-top: 3px;
        top: 0;
    }

    .item__info .item__name .indulgent {
        font-size: .8rem;
    }

    .item__info .item__name h5 {
        font-size: 1.5rem;
        margin-top: .2em;
    }

    .item__description .ingredients {
        font-size: .75rem;
    }

    .item__description {
        margin-left: 0;
    }

    .item__description p {
        font-weight: 100;
        line-height: 20px;
        position: relative;
        font-size: .8rem;
    }
}</style>