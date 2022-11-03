<template>
    <div class="card-section">
        <div class="card" v-for="item in content" :key="item.id" :style="{ backgroundColor: item.color }">
            <div class="top-card">
                <div class="text">
                    <h2>{{ item.title }}</h2>
                </div>
                <div class="image">
                    <img :src="item.img" />
                </div>
            </div>
            <div class="body-card">
                <div class="text">
                    <h3>{{ item.topic }}</h3>
                    <h3>{{ item.place }}</h3>
                    <h3>{{ item.major }}</h3>
                    <p>{{ item.distric }}</p>
                    <p>{{ item.since }}</p>
                    <p>{{ item.grade }}</p>
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
                    img: require('/assets/resumePhoto/1.png'),
                    title: "HIGH SCHOOL",
                    color: "#7DFFA2",
                    topic: "Pakphanang School",
                    place: "Intermediate school",
                    distric: "Nakhon sri thammarat",
                    major: "(Science and Mathematics Program)",
                    since: "2012-2017",
                    grade: "GPA: 2.98"
                },
                {
                    id: 2,
                    img: require('/assets/resumePhoto/2.png'),
                    title: "UNIVERSITY",
                    color: "#FA9483",
                    topic: "Faculty of Engineering",
                    place: "Prince of Songkla University",
                    distric: "Hatyai - Songkla",
                    major: "(Manufacturing Engineering)",
                    since: "2017-2021",
                    grade: "GPA: 2.40"
                },
                {
                    id: 3,
                    img: require('/assets/resumePhoto/3.png'),
                    title: "INTERNSHIP",
                    color: "#FFA600",
                    topic: "Design and develop website",
                    place: "Department of Engineer,",
                    major: "Prince of Songkla University",
                    since: "Develop website of Department of Industry Engineer with Joomla and PHP (2-month)",
                    distric: "Design website with Photoshop and used Figma for design"
                },
            ],

        }
    }
}
</script>

<style lang="scss">
.card-section {
    width: 100%;
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    align-items: center;

    .card {
        border: 1px solid white;
        width: 380px;
        height: 450px;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        background-color: white;
        border-radius: 40px;
        position: relative;

        .top-card {
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            position: relative;
            z-index: 3;
        }

        .image {
            width: 100px;
            height: 100px;


            img {
                width: 80%;
                height: 80%;
                background-color: #fff;
                border-radius: 50%;
                z-index: 2;
            }
        }

        .body-card {
            display: flex;
            flex-direction: column;
            background-color: #fff;
            border: 1px solid white;
            height: 320px;
            width: 380px;
            border-radius: 40px;
            position: absolute;
            bottom: 0px;
            z-index: 1;

            .text {
                margin-top: 40px;

                h3 {
                    display: flex;
                    justify-content: center;
                    margin: 15px;
                    padding: 0px;
                    letter-spacing: 1px;
                }

                p {
                    display: flex;
                    justify-content: center;
                    margin: 10px;
                    padding: 5px;
                    font-weight: 100;
                    font-size: 18px;
                    text-align: center;
                }
            }
        }
    }
}

@media only screen and (max-width:992px) and (min-width:601px) {
    .card-section {
        display: flex;
        flex-direction: column;


        .card {
            margin-bottom: 40px;
            display: flex;
            flex-direction: row;
            width: 700px;
            height: 250px;

            .top-card {
                .image {
                    position: absolute;
                    left: 160px;
                }

                .text {
                    width: 100%;
                    display: flex;
                    justify-content: center;
                    left: 85px;
                    position: absolute;

                    h2 {
                        text-align: center;
                        color: white;
                        text-shadow: 0px 0px 2px black;
                    }
                }
            }


            .body-card {
                height: 250px;
                width: 500px;
                position: absolute;
                right: 0px;

                .text {
                    margin: 0px;


                    h3 {
                        display: flex;
                        font-size: 16px;
                    }

                    p {
                        font-size: 14px;

                    }
                }
            }

        }

    }
}

@media only screen and (max-width:600px) {
    .card-section {
        display: flex;
        flex-direction: column;


        .card {
            width: 350px;
            height: 400px;
            margin-bottom: 40px;
            display: flex;
            flex-direction: column;
            position: relative;

            .image {
                width: 85px;
                height: 85px;

            }

            .body-card {

                height: 300px;
                width: 350px;

                .text {
                    margin-top: 35px;

                    h3 {
                        margin: 15px;
                        letter-spacing: 0;
                        font-size: 16px;
                    }

                    p {
                        margin: 5px;
                        font-size: 16px;
                    }
                }
            }
        }

    }
}
</style>