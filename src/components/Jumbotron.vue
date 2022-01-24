<template>
    <div class="jumbotron">
        <div class="icon">
            <div class="demos">
                <p><i class="fab fa-atlassian"></i></p>
                <p class="text-icon">Demos</p>
            </div>
            <div class="sale">
                <p><span class="dollar">$</span><span class="trentanove">39</span></p>
                <p class="text-icon">On Sale</p>
            </div>
        </div>
        <div class="jumbotron-text">
            <p class="pick">TODAY'S PICK</p>
            <div class="jumbotron-text-center">
            <h1>Food Corner: Top Jappanese Restaurant for Shushi</h1>
            <p>March 25, 2019</p>
            </div>
        </div>
    </div>
  
</template>

<script>
export default {
    name: 'Jumbotron'
}
</script>

<style lang="scss">
@import "../assets/scss/partials/_variables.scss";

    .jumbotron {
        height: 500px;
        background: url('../assets/images/single-post-img3-1200x790.jpg');
        background-size: cover;
        background-position-y: center;
        display: flex;
        justify-content: center;
        align-items: center;
        position: relative;
        .icon {
            
            position: absolute;
            top: -90px;
            right: 20px;

            .text-icon {
                font-size: 0.7em;
                color: $nevada;
            }

            .fa-atlassian {
                color: $fiord;
            }

            .demos, .sale {
                width: 55px;
                height: 55px;
                text-align: center;
                background-color: $springWood;
                margin-bottom: 0.5em;
                padding: 0.5em;
                font-family: $fontFamily;
                font-weight: bold;
                border-radius: 5px;
                box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
            }

            .sale {
                position: relative;

                .dollar, .trentanove {
                    color: $forestGreen;
                }

                .dollar {
                    position: absolute;
                    top: 5px;
                    left: 5px;
                }
                .trentanove {
                    font-size: 1.3em;
                }
            }

            
        }
    }

    .jumbotron-text {
        width: 40%;
        padding: 2em 0;
        background-color: $springWood;
        display: flex;
        justify-content: center;
        position: relative;
        border-radius: 10px;
        .pick {
            position: absolute;
            left: 50%;
            top: -15px;
            transform: translate(-50%);
            padding: 5px 15px;
            font-size: 0.7em;
            font-weight: bold;
            background-color: $orange;
            border-radius: 5px;
            font-family: $fontFamily;
            color: $springWood;
        }
        .jumbotron-text-center {
            width: 80%;
            h1 {
                text-align: center;
            }
            p {
                padding-top: 1em;
                text-align: center;
                color: $nevada;
            }
        }
    }
</style>