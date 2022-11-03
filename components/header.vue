<template>
    <div class="container">
        <div class="header-bar">
            <div class="left">
                <div class="circle">
                </div>
                <div class="name">
                    <button @click="toggleActive">
                        <a href="#section1">PORAMIN KEERINNON</a>
                    </button>
                </div>
            </div>
            <div class="right">
                <div class="left-item">
                    <a href="#section2">RESUME</a>
                </div>
                <div class="middle-item">
                    <a href="#section3">SKILLS</a>
                </div>
                <div class="right-item">
                    <a href="#section4">CONTACT</a>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            statusList: [
                {
                    id: 1,
                    name: "RESUME",
                    active: true,
                },
                {
                    id: 2,
                    name: "SKILLS",
                    active: true,
                },
                {
                    id: 3,
                    name: "CONTACT",
                    active: true,
                }
            ]
        }
    },
    methods: {

    }
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=IBM+Plex+Sans:ital,wght@0,400;0,600;1,700&display=swap');

.container {
    display: flex;
    align-items: center;
    margin: 0;
    padding: 0px;
    font-family: 'IBM Plex Sans', sans-serif;
    z-index: 10;


    h4 {
        padding: 0;
        margin: 0;

    }

    .header-bar {
        background-color: #F7D07A;
        border-radius: 50px;
        display: flex;
        flex-direction: row;
        width: 95%;
        height: 60px;
        justify-content: space-between;
        position: absolute;
        top: 30px;
        visibility: show;

        .left {
            display: flex;
            flex-direction: row;
            justify-content: center;
            align-items: center;
            position: relative;

            .circle {
                width: 30px;
                height: 30px;
                border-radius: 50%;
                background-color: #293242;
                margin-left: 40px; //*** */
            }

            .name {
                button {
                    display: flex;
                    flex-direction: row;
                    padding: 0px;
                    font-weight: 600;
                    letter-spacing: 5px;
                    color: #293242;
                    background-color: #F7D07A;
                    margin: 15px; //*** */
                    padding: 7px; //*** */
                    border: none;

                    a {
                        padding: 10px;
                        text-decoration: none;
                        color: #293242;
                        font-size: 22px;
                    }
                }
            }
        }

        .right {
            display: flex;
            flex-direction: row;
            justify-content: flex-end;
            align-items: center;
            padding-right: 40px; //*** */
            font-weight: 300;
        }

        .name:hover {
            background-color: #293242;
            height: 60px;
            display: flex;
            width: 400px;
            justify-content: center;
            align-items: center;
            padding: 0px;
            margin: 15px; //*** */
            overflow: hidden;
            transition: 0.5s;

            button:hover {
                background-color: #293242;

                a:hover {
                    color: white;
                }
            }

        }

        .right>div {
            padding: 0px 20px 0px 20px;
            font-size: 20px;
            letter-spacing: 2px;
            border-right: 2px solid white;
            font-weight: 300;

            a {
                text-decoration: none;
                font-weight: 300;
                color: black;
                text-shadow: 0px 0px 2px white;
            }
        }

        .right>div:hover {
            background-color: #293242;
            padding: 17px; //*** */
            transform: scale(1.1);
            overflow: hidden;
            transition: 0.5s;

            a {
                color: white;
            }
        }
    }

}

@media only screen and (max-width:600px) {
    .header-bar {
        visibility: hidden;
    }
}

@media only screen and (max-width:992px) {
    .header-bar {
        visibility: hidden;
    }
}
</style>