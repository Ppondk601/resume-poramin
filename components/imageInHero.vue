<template>
    <div class="container">
        <div class="image">
            <img src="~assets/heroPhoto/IMG_5588.jpg">
        </div>


    </div>
</template>

<script>
export default {
    data() {
        return {
        }
    }
}
</script>

<style lang="scss">
.container {
    display: flex;
    flex-direction: row;
    align-items: center;

    div {
        margin: 0%;
        padding: 0;
    }

    .image {
        img {
            width: 400px;
            height: 330px;
            border-radius: 30px;
            border: 5px solid white;
            opacity: 90%;
            filter: brightness(110%);
        }
    }

    @media only screen and (max-width:600px) {
        .image {
            img {
                width: 260px;
                height: 210px;
                border-radius: 40px;

            }
        }
    }

    @media only screen and (max-width:992px) and (min-width:601px) {
        .image {
            img {
                width: 280px;
                height: 250px;
                border-radius: 40px;
                margin-left: 1%; //*** */
            }
        }
    }
}
</style>