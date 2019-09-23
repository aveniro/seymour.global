<template>
    <div class="skill">
        <div class="title"><slot></slot></div>
        <div ref="level" class="level"></div>
    </div>
</template>

<script>
    export default {
        props: {
            level: {
                type: Number,
                default: 0
            }
        },
        mounted() {
            this.$refs.level.style.background = `linear-gradient(to right, #00a1ff ${(this.level / 5)*100}%, gray ${100 - (this.level / 5)*100}%)`;
        }
    }
</script>

<style lang="scss" scoped>
    .skill {
        margin-top: 1em;

        .title {
            font-size: 13px;
            font-weight: 400;
        }

        .level {
            height: 5px;
            margin-top: 0.5em;
            background: black;
        }
    }
</style>