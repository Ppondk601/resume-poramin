<template>

    <div class="contact-section">
        <div class="itemInContact">
            <div class="first-item">
                <a href="https://www.facebook.com/poramin.keerinnon">
                    <font-awesome-icon :icon="['fab', 'facebook']" />
                    Facebook
                </a>
            </div>
            <div class="second-item">
                <a href="https://www.linkedin.com/in/poramin-keerinnon-193560237/">
                    <font-awesome-icon :icon="['fab', 'linkedin']" /> Linkedin
                </a>
            </div>
            <div class="third-item">
                <a href="">
                    <font-awesome-icon :icon="['fab', 'line']" />
                    Line
                </a>
            </div>
            <div class="forth-item">
                <a href="https://github.com/Ppondk601">
                    <font-awesome-icon :icon="['fab', 'github']" />
                    Github
                </a>
            </div>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style lang="scss">
.contact-section {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    color: white;
    width: 100%;

    .itemInContact {
        display: flex;
        flex-direction: row;

        .first-item {
            color: white;
            padding: 40px;
        }

        .first-item:hover {
            transform: scale(1.5);
            transition: 1s;

            a:hover {
                color: #4267B2;
                transition: 0.5s;
                text-shadow: 0.5px 0.5px white;
            }
        }

        .second-item {
            padding: 40px;
        }

        .second-item:hover {
            transform: scale(1.5);
            transition: 1s;

            a:hover {
                color: #0072b1;
                transition: 0.5s;
                text-shadow: 0.5px 0.5px white;
            }

        }

        .third-item {
            padding: 40px;
        }

        .third-item:hover {
            transform: scale(1.5);
            transition: 1s;

            a:hover {
                color: #00b900;
                transition: 0.5s;
                text-shadow: 0.5px 0.5px white;
            }

        }

        .forth-item {
            padding: 40px;
        }

        .forth-item:hover {
            transform: scale(1.5);
            transition: 1s;

            a:hover {
                color: #f5f5f5;
                transition: 1.0s;
                text-shadow: 1px 1px black;

            }
        }
    }

    *>div {
        font-size: 24px;

        a {
            text-decoration: none;
            color: white;
            font-weight: 600;
            font-style: italic;
        }
    }
}

@media only screen and (max-width:600px) {
    .contact-section {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;

        .itemInContact {
            display: flex;
            flex-direction: column;
            padding: 0px;
            margin: 0px;

            .first-item {
                padding: 10px;
            }

            .second-item {

                padding: 10px;
            }

            .third-item {

                padding: 10px;
            }

            .forth-item {

                padding: 10px;
            }
        }

    }
}
</style>