<template>
    <div class="testimonial">
        <div class="body">
            "<slot></slot>"
        </div>
        <div class="name">
            -{{ from }}
        </div>
    </div>
</template>

<script>
    export default {
        props: {
            from: {
                type: String,
                default: ""
            }
        }
    }
</script>

<style lang="scss" scoped>
    .testimonial {
        background: white;
        filter: brightness(0.99);

        border: rgba(gray, 0.5) 1px solid;
        border-radius: 0.2em;

        padding: 1em;

        line-height: 1.5em;

        .body {
            font-style: italic;
        }

        .name {
            margin-top: 1em;
            text-align: right;
        }
    }
</style>