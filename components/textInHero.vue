<template>
    <div>
        <div class="text-box">
            <div class="name">
                <div class="first-name">
                    <h2>PORAMIN</h2>
                </div>
                <div class="last-name">
                    <h2>KEERINNON</h2>
                </div>
            </div>
            <div class="position">
                <h4>JUNIOR</h4>
                <h4>FRONTEND</h4>
                <h4>DEVELOP</h4>
            </div>

            <div class="quote">
                <p>Life is an adventure! So live it up!</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style lang="scss">
.text-box {
    display: flex;
    flex-direction: column;
    margin: 0;

    .name {
        display: flex;
        flex-direction: row;
        font-weight: 600;
        font-size: 28px;
        letter-spacing: 4px;
        color: white;
        margin: 0px;
        justify-content: center;
        text-shadow: 0 0 3px white;

        .last-name {
            padding-left: 5%;
        }
    }

    .position {
        display: flex;
        flex-direction: row;
        justify-content: center;

        h4 {
            color: #7FFFBF;
            padding-left: 2%;
            font-size: 26px;
            letter-spacing: 2px;
            font-weight: 300;
            text-shadow: 0 0 2.5px white;
        }
    }

    .quote {
        color: white;
        padding-left: 2%;
        font-size: 24px;
        letter-spacing: 2px;
        font-weight: 300;
        align-self: center;
        padding: 5px 0px 20px 0px;
    }
}

@media only screen and (max-width:992px) and (min-width:601px) {
    .text-box {
        display: flex;
        padding: 0;


        .name {
            font-size: 18px;
            letter-spacing: 4px;
        }

        .position {
            h4 {
                font-size: 18px;
            }

        }

        .quote {
            font-size: 17px;

        }
    }

}

@media only screen and (max-width:600px) {
    .text-box {
        display: flex;
        padding: 0;


        .name {
            font-size: 16px;
            letter-spacing: 3px;
        }

        .position {
            h4 {
                font-size: 16px;
            }

        }

        .quote {
            font-size: 15px;

        }
    }

}
</style>