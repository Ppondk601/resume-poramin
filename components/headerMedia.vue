<template>
    <div class="header-hidden">
        <div class="item-hidden">
            <div class="menu">
                <button @click="dropdown">
                    <div class="filterHandle" v-if="active"></div>
                    <i>
                        <font-awesome-icon :icon="['fas', 'bars']" />
                    </i>
                </button>

                <div class="item" v-if="active">
                    <a href="#section1">Home</a>
                </div>
                <div class="item" v-if="active">
                    <a href="#section2">Resume</a>
                </div>
                <div class="item" v-if="active">
                    <a href="#section3">Skills</a>
                </div>
                <div class="item" v-if="active">
                    <a href="#section4">Contact</a>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            active: false
        }
    },
    methods: {
        dropdown() {
            this.active = !this.active
        }
    }
}
</script>

<style lang="scss">
.header-hidden {
    display: flex;
    width: 100%;
    position: relative;



    .item-hidden {
        display: flex;
        flex-direction: column;

        .menu {
            .filterHandle {
                display: flex;
                width: 100%;
                height: 3158px;
                background-color: rgba(0, 0, 0, 0.177);
                backdrop-filter: blur(3px);
                margin: 0px;
                padding: 0px;
                position: absolute;
                top: -3%; //*** */
                left: -1%; //*** */
                z-index: -1;
            }

            button {
                display: flex;
                flex-direction: row;
                margin: 0;
                padding: 30px; //*** */
                border: none;
                z-index: 5;

                p {
                    margin: 0;
                }
            }

            .item {
                display: flex;
                justify-content: center;
                align-items: center;
                margin: 0;
                padding: 0;
                background-color: rgba(0, 0, 0, 0.638);
                z-index: 5;

                a {
                    text-decoration: none;
                    color: white;
                    text-shadow: 0px 0px 3px black;
                    font-weight: 600;
                    padding: 22px; //*** */
                }
            }

            .item:hover {
                background-color: #F7D07A;

                a {
                    color: black;
                }
            }
        }
    }

}

@media only screen and (max-width:992px) and (min-width:601px) {
    .header-hidden {
        display: flex;
        justify-content: flex-start;
        width: 100%;
        margin-left: auto;
        margin-right: auto;
        position: relative;

        .menu {
            width: 100%;
            display: flex;
            flex-direction: column;
            justify-content: center;
            position: absolute;
            left: -2.5%;

            button {
                padding: 20px;
                margin-left: 0;
                font-size: 25px;
                color: white;
                background-color: #29324200;
            }

            i:hover {
                transform: scale(1.3);
                transition-duration: 0.8;
            }

            .item {
                width: 100%;
                width: 992px;
                display: flex;

                a {
                    font-size: 20px;
                    display: flex;
                    justify-content: center;
                }

                animation: growDown 700ms ease-in-out forwards;

                transform-origin: top center;

                @keyframes growDown {
                    0% {
                        opacity: 0;
                        transform: scale(0);
                    }

                    80% {
                        transform: scale(1.07);
                    }

                    100% {
                        opacity: 1;
                        transform: scale(1);
                    }
                }
            }
        }
    }

}

@media only screen and (max-width:600px) {
    .header-hidden {
        display: flex;
        justify-content: flex-start;
        width: 600px;
        position: relative;

        .menu {
            position: absolute;
            left: -8%;


            button {
                padding: 20px;
                margin-left: 10%; //*** */
                font-size: 25px;
                color: white;
                background-color: #29324200;
                z-index: 5;
            }

            i:hover {
                transform: scale(1.3);
                transition-duration: 0.8;
            }

            .item {
                display: flex;
                justify-content: center;
                align-items: center;
                width: 100%;
                width: 600px;
                z-index: 5;


                a {
                    font-size: 20px;
                    display: flex;
                    justify-content: center;

                }

                animation: growDown 700ms ease-in-out forwards;

                transform-origin: top center;

                @keyframes growDown {
                    0% {
                        opacity: 0;
                        transform: scale(0);
                    }

                    80% {
                        transform: scale(1.07);
                    }

                    100% {
                        opacity: 1;
                        transform: scale(1);
                    }
                }
            }
        }
    }
}
</style>