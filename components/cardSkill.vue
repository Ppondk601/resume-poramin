<template>
    <div class="section-skill">
        <div class="cardSkill" v-for="item in content" :key="item.id">
            <div class="item-front">
                <div class="image">
                    <img :src="item.image" />
                </div>
                <div class="text">
                    <p> {{ item.name }}</p>
                </div>
            </div>
            <div class="item-back">
                <div class="title">
                    <p>LEVEL</p>
                </div>
                <div class="scale" :style="{ height: item.height, backgroundColor: item.color }">
                    <p>{{ item.scale }}</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            content: [
                {
                    id: 1,
                    image: require('/assets/skillPhoto/css.png'),
                    name: 'CSS',
                    scale: "FLUENT",
                    height: "80%",
                    color: "#77DD77",
                },
                {
                    id: 2,
                    image: require('/assets/skillPhoto/html.png'),
                    name: "HTML",
                    scale: "FLUENT",
                    height: "80%",
                    color: "#77DD77",
                },
                {
                    id: 3,
                    image: require('/assets/skillPhoto/JS.png'),
                    name: "Javascript",
                    scale: "FAIR",
                    height: "55%",
                    color: "#F7D07A",

                },
                {
                    id: 4,
                    image: require('/assets/skillPhoto/C++ icon.png'),
                    name: "C++",
                    scale: "FAIR",
                    height: "50%",
                    color: "#F7D07A",

                },
                {
                    id: 5,
                    image: require('/assets/skillPhoto/vue.png'),
                    name: "Vue.js",
                    scale: "FAIR",
                    height: "55%",
                    color: "#F7D07A",

                },
                {
                    id: 6,
                    image: require('/assets/skillPhoto/nuxt.png'),
                    name: "Nuxt.js",
                    scale: "FAIR",
                    height: "55%",
                    color: "#F7D07A"

                },
                {
                    id: 7,
                    image: require('/assets/skillPhoto/figma.png'),
                    name: "Figma",
                    scale: "GOOD",
                    height: "65%",
                    color: "#DAFAB1"

                },
                {
                    id: 8,
                    image: require('/assets/skillPhoto/firebase.png'),
                    name: "Firebase",
                    scale: "FAIR",
                    height: "50%",
                    color: "#F7D07A"

                }

            ]
        }
    }
}
</script>

<style lang="scss">
.section-skill {
    display: flex;
    flex-wrap: wrap;
    flex-direction: row;
    width: 90%;
    height: 50%;
    justify-content: space-between;
    align-items: center;


    .cardSkill {
        display: flex;
        flex-direction: row;
        background-color: transparent;
        width: 300px;
        height: 200px;
        perspective: 1000px;
        transition: transform 1s;
        transform-style: preserve-3d;
        padding-bottom: 30px;

        .item-front,
        .item-back {
            position: absolute;
            width: 100%;
            height: 100%;
            backface-visibility: hidden;
        }

        .item-front {
            width: 200px;
            height: 200px;
            justify-content: center;
            align-items: center;
            display: flex;
            flex-direction: column;
            background-color: #293242;
            border-radius: 30px;
            margin: 30px 30px 0px 30px;

            .image {

                img {
                    width: 100px;
                    height: 100px;
                    border: none;
                }
            }

            .text {
                p {
                    color: white;
                    font-weight: 600;
                    font-size: 18px;
                    text-shadow: 0px 0px 1px white;
                }
            }
        }

        .item-back {
            width: 200px;
            height: 200px;
            border-radius: 30px;
            justify-content: center;
            align-items: center;
            display: flex;
            flex-direction: column;
            transform: rotateY(-180deg);
            background-color: #293242;
            margin: 30px 20px 30px 70px;
            position: relative;
            border: 2px solid black;

            .title {
                display: flex;
                padding: 0px;
                margin: 0px;
                position: absolute;
                top: 10px;
                width: 60%;
                z-index: 5;
                justify-content: center;
                height: 20%;
                border-radius: 30px;
                background-color: rgba(255, 255, 255, 0.97);
                align-items: center;

                p {
                    color: black;
                }
            }

            .scale {
                display: flex;
                width: 100%;
                border-radius: 0px 0px 30px 30px;
                justify-content: center;
                align-items: center;
                position: absolute;
                bottom: 0px;
                z-index: 1;

                p {
                    text-shadow: 1px 1px 3px black;
                }

            }


            p {
                color: white;
                font-weight: 600;
                font-size: 24px;
            }
        }


        .item-front:hover {
            background-color: #fff;
        }
    }

    .cardSkill:hover {
        transform: rotateY(-180deg);
    }


}

@media only screen and (max-width:992px) and (min-width:601px) {
    .section-skill {
        display: grid;
        grid-template-rows: auto auto auto;
        grid-template-columns: auto auto auto;
        align-items: center;
        justify-content: center;
    }
}

@media only screen and (max-width:600px) {
    .section-skill {
        display: grid;
        grid-template-rows: auto auto auto auto;
        grid-template-columns: auto auto;
        align-items: center;
        justify-content: center;



        .cardSkill {
            width: 250px;
            height: 150px;
            margin: 1% -2% 1% -2%;
            padding: 0px;
            display: flex;
            justify-content: center;
            align-items: center;

            .item-front {
                width: 150px;
                height: 150px;

                .image {
                    img {
                        width: 80px;
                        height: 80px;
                    }
                }
            }

            .item-back {
                width: 150px;
                height: 150px;
                margin: 0px;
            }
        }
    }
}
</style>