<template>
    <div class="container">
        <div class="top-button">
            <button>
                <p>LET START</p>
            </button>
        </div>

        <div class="under-button">
            <div class="button-left">
                <a href="#section2">
                    RESUME
                </a>
            </div>
            <div class="button-mid">
                <a href="#section3">
                    SKILLS
                </a>
            </div>
            <div class="button-right">
                <a href="#section4">
                    CONTACT
                </a>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {

        }
    },
}
</script>

<style lang="scss">
.container {
    display: flex;
    flex-direction: column;
    padding: 50%;

    .top-button {
        margin: 0;
        padding: 0px;
        font-family: 'IBM Plex Sans', sans-serif;
        visibility: visible;

        button {
            border-radius: 0px;
            background-color: #7FFFBF;
            width: 190px;
            border-radius: 50px;
            height: 80px;
            font-weight: 600;
            font-size: 22px;
            letter-spacing: 2px;
            color: #293242;

        }
    }

    .under-button {
        display: flex;
        flex-direction: row;

        .button-left {

            a {
                display: flex;
                height: 90px;
                width: 90px;
                border-radius: 50px;
                letter-spacing: 50%;
                font-weight: 400;
                letter-spacing: 1.5px;
                background-color: #FA9483;
                text-decoration: none;
                justify-content: center;
                align-items: center;
                overflow: hidden;
                color: white;

            }
        }

        >* {
            height: 90px;
            width: 90px;
            border-radius: 50px;
            margin: 30px 40px 0px 40px;
            letter-spacing: 50%;
            font-weight: 400;
            letter-spacing: 1.5px;
            border: none;
        }

        .button-mid {
            background-color: #4097AA;
            color: white;

            a {
                display: flex;
                height: 90px;
                width: 90px;
                border-radius: 50px;
                letter-spacing: 50%;
                font-weight: 400;
                letter-spacing: 1.5px;
                background-color: #4097AA;
                text-decoration: none;
                justify-content: center;
                align-items: center;
                overflow: hidden;
                color: white;
            }
        }

        .button-right {
            background-color: #58508D;
            color: white;

            a {
                display: flex;
                height: 90px;
                width: 90px;
                border-radius: 50px;
                letter-spacing: 50%;
                font-weight: 400;
                letter-spacing: 1.5px;
                background-color: #58508D;
                text-decoration: none;
                justify-content: center;
                align-items: center;
                overflow: hidden;
                color: white;

            }
        }

        a:hover {
            opacity: 1;
            transform: scaleX(1.2) scaleY(1.2);
            transition: 0.7s;
            background-color: #fff;
            color: black;
            font-weight: 600;
        }
    }
}

@media only screen and (max-width:992px) and (min-width:601px) {
    .container {
        padding: 0%;

        .top-button {
            visibility: hidden;
        }

        .under-button {


            >* {
                height: 60px;
                width: 60px;
                border-radius: 50%;
                margin: 30px 40px 0px 40px;
                letter-spacing: 50%;
                font-weight: 400;
                letter-spacing: 1.5px;
                border: none;
            }

            .button-left {
                a {
                    height: 60px;
                    width: 60px;
                    border-radius: 50%;
                    font-size: 12px;
                }
            }

            .button-mid {
                a {
                    height: 60px;
                    width: 60px;
                    border-radius: 50%;
                    font-size: 12px;
                }
            }

            .button-right {
                a {
                    height: 60px;
                    width: 60px;
                    border-radius: 50%;
                    font-size: 12px;
                }
            }

        }
    }
}

@media only screen and (max-width:600px) {
    .container {
        padding: 0%;

        .top-button {
            visibility: hidden;
        }

        .under-button {


            >* {
                height: 60px;
                width: 60px;
                border-radius: 50%;
                margin: 30px 40px 0px 40px;
                letter-spacing: 50%;
                font-weight: 400;
                letter-spacing: 1.5px;
                border: none;
            }

            .button-left {
                a {
                    height: 60px;
                    width: 60px;
                    border-radius: 50%;
                    font-size: 12px;
                }
            }

            .button-mid {
                a {
                    height: 60px;
                    width: 60px;
                    border-radius: 50%;
                    font-size: 12px;
                }
            }

            .button-right {
                a {
                    height: 60px;
                    width: 60px;
                    border-radius: 50%;
                    font-size: 12px;
                }
            }

        }
    }
}
</style>