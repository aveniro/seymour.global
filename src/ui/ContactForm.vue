<template>
    <div class="contact-form">
        <form action="https://api.seymour.global/contact" method="POST">
            <input name="name" type="text" class="name" placeholder="Name">
            <input name="email" type="text" class="email" placeholder="Email Address">
            <textarea name="message" type="textarea" class="body" placeholder="Message body..."></textarea>

            <input type="submit" value="Hire me!" class="send-btn">
        </form>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss" scoped>
    .contact-form {
        padding: 2em;
        width: 100%;
        background: rgba(black, 0.05);
        border-radius: 0.25em;
        box-shadow: 1px 1px 6px 3px rgba(black, 0.1);

        form {
            display: flex;
            flex-direction: column;

            input, textarea {
                margin-bottom: 1em;
                border-radius: 0.2em;
            }

            input[type="text"] {
                height: 3em;
            }

            textarea {
                height: 9em;
                resize: none;
            }

            textarea,
            input[type="text"] {
                padding: 1em;
                font-size: 14px;   
            }

            input[type="submit"] {
                height: 2.5em;
                cursor: pointer;
                margin: 1em 0 0 0;
                font-size: 18px;
                transition: 300ms;
                background: rgb(0, 153, 255);
                color: white;
                font-weight: 1000;

                &:hover {
                    filter: brightness(0.98);
                }

                &:active {
                    filter: brightness(0.95);
                }
            }
        }
    }
</style>