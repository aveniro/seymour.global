<template>
    <div id="app">
        <div class="nav">
            <div class="site-links">
                <a @click="nav('testimonials')">References</a>
                <a @click="nav('resume')">Resume</a>
            </div>
            <div class="outbound">
                <a href="https://www.italki.com/teacher/5358674/german" target="_blank">
                    <img src="./assets/icons/italki.svg" alt="">
                </a>
                <a href="https://github.com/NateSeymour" target="_blank">
                    <img src="./assets/icons/icons8-github.svg" alt="">
                </a>
                <a href="https://www.upwork.com/o/profiles/users/_~01b9ab3ded1cc08d25/" target="_blank">
                    <img src="./assets/icons/icons8-upwork.svg" alt="">
                </a>
                <a href="mailto:nathan@seymour.global" target="_blank">
                    <img src="./assets/icons/icons8-email_open_filled.svg" alt="">
                </a>
            </div>
        </div>

        <router-view />
    </div>
</template>

<script>
    export default {
        methods: {
            nav(selector) {
                document.getElementsByClassName(selector)[0].scrollIntoView({ behavior: 'smooth' });
            }
        }
    }
</script>

<style lang="scss">
    @import url('https://fonts.googleapis.com/css?family=Lato&display=swap');

    * {
        box-sizing: border-box;
        outline: none;
        border: none;
        margin: 0;
        padding: 0;

        font-family: 'Lato', sans-serif;
    }

    .nav {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: space-between;

        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 4em;

        background: rgba(black, 0.85);

        z-index: 1000;

        .site-links {
            a {
                text-decoration: none;
                color: white;
                font-size: 18px;

                margin: 0 1em 0 1em;
                cursor: pointer;

                user-select: none;

                &:hover {
                    filter: brightness(0.98);
                }

                &:active {
                    filter: brightness(0.95);
                }
            }
        }

        .outbound {
            display: flex;
            flex-direction: row;
            margin-right: 1em;

            a {
                width: 1.8em;
                height: 1.8em;
                margin: 0 0.5em 0 0.5em;

                img {
                    height: 100%;
                    width: 100%;

                    filter: brightness(0.8);

                    transition: 300ms;

                    &:hover {
                        filter: brightness(0.9);
                    }
                }
            }
        }
    }

    @media only screen and (max-width: 1000px) {
        .nav {
            .site-links {
                a {
                    font-size: 13px;
                }
            }

            .outbound {
                a {
                    height: 1.5em;
                    width: 1.5em;
                }
            }
        }
    }
</style>