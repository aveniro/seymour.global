<template>
    <div class="home">
        <div class="card beautiful">
            <CoolSlider />
        </div>

        <div class="card testimonials">
            <div class="left">
                <Testimonial from="Christian">No words... he is very competent. He has a great German pronuntiation (I felt like among german people). He is young but very good at teaching. Especially, he is veeeeery patient. Thanks, Nathan, and see you the next time.</Testimonial>
                <Testimonial from="Bridget">The lesson was great. Nathan is good about seizing opportunities to provide vocabulary and grammar lessons within the conversation.</Testimonial>
                <Testimonial from="Justin">Nathan was very punctual and his grammar and language ability was very impressive. He helped me on my homework while we also spoke in german. He also was very supportive, knowledgeable, and patient! Great teacher!</Testimonial>
                <Testimonial from="Cheryl">My favorite teacher on italki!</Testimonial>
            </div>

            <div class="right">
                <ContactForm />
            </div>
        </div>

        <div class="card resume">
            <div class="resume-body">
                <div class="basic-information"> 
                    <div class="name"> Nathan Seymour </div>
                </div>

                <div class="section">
                    <div class="title">Work Experience</div>

                    <div class="subtitle">Italki: German, English Teacher (Aug. 2018 - Present)</div>
                    <div class="text-body">
                        Five star language teacher on Italki for now over one year. With more than 40 students I have experience creating lesson plans, correcting grammar, engaging students in language learning materials and providing them with the tools to continue learning on their own. 
                    </div>

                    <div class="subtitle">Freelance: German, English, Spanish Translation (Present)</div>
                    <div class="text-body">
                        With native-level English and German abilities and an advanced knowledge of Spanish, I always deliver high quality translations. Due to my deep interest in computer science, I specialize in technical translations.
                    </div>
                </div>

                <div class="section">
                    <div class="title">Education</div>

                    <div class="subtitle">The Linsly School</div>
                    <div class="text-body">
                        I recieved my high school diploma from The Linsly School of Wheeling, WV. There, I excelled in my classes and graduated with a 4.0 grade point average, finishing at the top of my class in Spanish.
                    </div>

                    <div class="subtitle">Christophorusschule Oberurff</div>
                    <div class="text-body">
                        At the Christophorusschule Oberurff, I specialized in physics and German.
                    </div>

                    <div class="subtitle">Adolf Reichweinschule</div>
                    <div class="text-body">
                        At the Adolf Reichweinschule, I recieved education in software development and the fundamentals of programming.
                    </div>
                </div>

                <div class="section">
                    <div class="title">Interests</div>

                    <div class="subtitle">Web Development</div>
                    <div class="text-body">
                        A lot of my freetime is framed in by web development, one of my biggest hobbies. I built the website that you are using now using some of the industry's latest technologies: ESNext, Vue, Webpack and SCSS.
                    </div>

                    <div class="subtitle">Writing</div>
                    <div class="text-body">
                        When I'm not programming, you can probably find me writing. <a href="https://medium.com/@nathan_seymour" target="_blank">Check out my Medium page for more information.</a>
                    </div>
                </div>
            </div>
            
            <div class="right-panel">
                <div class="contact">
                    <div class="title"> Contact </div>

                    <a href="mailto:nathan@seymour.global">
                        <img src="../assets/icons/icons8-email_open_filled.svg" alt="">
                        nathan@seymour.global
                    </a>

                    <a href="tel:+13305757459">
                        <img src="../assets/icons/icons8-phone_filled.svg" alt="">
                        +1 (330) 575-7459
                    </a>

                    <a href="https://goo.gl/maps/NA3hmyz8A4G4A4Bz8" target="_blank">
                        <img src="../assets/icons/icons8-worldwide_location_filled.svg" alt="">
                        Madrid, Spain
                    </a>
                </div>

                <div class="section languages">
                    <div class="title"> Languages </div>

                    <Skill :level="5"> English </Skill>
                    <Skill :level="5"> German </Skill>
                    <Skill :level="4"> Spanish </Skill>
                </div>

                <div class="section skills">
                    <div class="title"> Skills </div>

                    <Skill :level="4"> Translation </Skill>
                    <Skill :level="4"> Teaching </Skill>
                </div>

                <div class="section">
                    <div class="title">Certifications</div>

                    <div class="cert">- Goethe Certificate C2</div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import Testimonial from '@/ui/Testimonial.vue';
    import Skill from '@/ui/Skill.vue';
    import CoolSlider from '@/ui/CoolSlider.vue';
    import ContactForm from '@/ui/ContactForm.vue';

    export default {
        components: { Testimonial, Skill, CoolSlider, ContactForm }
    }
</script>

<style lang="scss" scoped>
    .card {
        width: 100vw;
        height: 100vh;
    }

    .beautiful {
        background-image: url("../assets/NathanSeymour.jpg");
        background-size: cover; /* or contain depending on what you want */
        background-position: center center;
        background-repeat: no-repeat;
    }

    .testimonials {
        padding: 1.5em;
        display: flex;
        flex-direction: row;

        height: auto;

        .left {
            padding: 3em;

            width: 50%;

            .testimonial {
                margin: 1em;
            }
        }
        
        .right {
            display: flex;
            align-items: center;
            padding: 6em;
            width: 50%;
        }
    }

    .title {
        font-size: 20px;
        font-weight: 600;
    }

    .subtitle {
        font-size: 16px;
        font-weight: 600;
        margin-top: 1.5em;
    }

    .text-body {
        margin-top: 1em;
        font-size: 13px;
        max-width: 75%;
    }

    .cert {
        margin-top: 0.5em;
        font-size: 14px;
    }

    .section {
        margin-top: 3em;
    }

    .resume {
        height: auto;
        padding: 5em;
        background: rgba(black, 0.05);

        display: flex;
        flex-direction: row;

        .resume-body {
            flex-grow: 1000;

            .basic-information {
                .name {
                    font-size: 25px;
                    font-weight: 600;
                }
                .age {}
            }
        }
        
        .right-panel {
            min-width: 20%;

            .contact {
                a {
                    margin-top: 0.5em;
                    text-decoration: none;
                    align-items: center;
                    display: block;

                    img {
                        height: 1em;
                        width: 1em;

                        filter: brightness(0.1);
                    }
                }
            }
        }
    }

    @media only screen and (max-width: 1000px) {
        .home {
            .testimonials {
                flex-direction: column;
                padding: 1em;

                .left {
                    width: 100%;
                    padding: 0;
                }

                .right {
                    width: 100%;
                    padding: 1em;
                }
            }

            .text-body {
                max-width: 100%;
            }

            .resume {
                flex-direction: column-reverse;
                padding: 2em;

                .right-panel {
                    margin-bottom: 3em;
                }
            }
        }
    }
</style>