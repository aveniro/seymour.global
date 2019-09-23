<template>
    <div class="cool-slider">Slider</div>
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss" scoped>
    .cool-slider {
        position: absolute;

        top: 4.5em;
        left: 2.5em;

        background: black;

        border: 5px solid white;

        width: 15em;

        color: transparent;

        padding: 0.5em;
        font-size: 35px;

        user-select: none;

        transition: 500ms;

        &::after {
            content: 'Nathan Seymour';
            position: absolute;
            top: 0;
            left: 0;
            color: white;
            opacity: 1;
            padding: 0.5em;
            animation: change 10s linear alternate infinite;
        }
    }

    @keyframes change {
        0% {
            color: white;
            content: 'Nathan Seymour';
        }

        25% {
            color: black;
        }

        50% {
            color: white;
            content: 'Professional Translator';
        }

        75% {
            color: black;
        }

        100% {
            color: white;
            content: 'Language Teacher';
        }
    }

    @media only screen and (max-width: 1000px) {
        .cool-slider {
            left: 1em;
            top: 7em;
            font-size: 20px;
        }
    }
</style>