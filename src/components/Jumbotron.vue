<template>
    <div class="jumbotron-tot">
        <div class="jumbotron">
            <img :src="journals[0].img" alt="">
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
            <div class="foodie-journal">
                <h5>FOODIE JOURNAL</h5>
                <ul>
                    <li v-for="(journal, index) in journals"
                        :key= "index">
                        <div class="img-jumbotron">
                            <img :src="journal.img" alt="">
                            <div class="hover">
                                <i class="fas fa-link"></i>
                                <p>{{ journal.text }}</p>
                            </div> 
                        </div>
                        <h4>{{ journal.text }}</h4>
                        <p class="data">{{ journal.admin }}</p>
                    </li>
                </ul>
            </div>
        </div>

    </div>
  
</template>

<script>
export default {
    name: 'Jumbotron',
    data() {
        return {
            journals: [
                {
                    img: require('../assets/images/single-post-img3-1200x790.jpg'),
                    text: 'Food Corner: Top Japanese restaurant for Sushi',
                    admin: 'By Admin | March 25th 2019'
                },
                {
                    img: require('../assets/images/fi-roundup-1200x790.jpg'),
                    text: 'Roundup: My New Favourite Recipes For Heathy Living',
                    admin: 'By Admin | March 25th 2019'
                },
                {
                    img: require('../assets/images/fi-toasts-1200x790.jpg'),
                    text: 'Why These Toast with Tea Are My New Favourite',
                    admin: 'By Admin | March 25th 2019'
                }
            ],
        }
    }
}
</script>

<style lang="scss">
@import "../assets/scss/partials/_variables.scss";

    .jumbotron-tot {
        width: 100%;
        height: 750px;
        background-color: $cararra;
    }

    .jumbotron {
        height: 500px;
        position: relative;
        img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

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

            .demos,
            .sale {
                width: 55px;
                height: 55px;
                text-align: center;
                background-color: white;
                margin-bottom: 0.5em;
                padding: 0.5em;
                font-family: $fontFamily;
                font-weight: bold;
                border-radius: 5px;
                box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
            }

            .sale {
                position: relative;

                .dollar,
                .trentanove {
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
        .jumbotron-text {
            position: absolute;
            bottom: 50%;
            left: 50%;
            transform: translate(-50%,-50%);
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

        .foodie-journal {
            position: absolute;
            top: 80%;
            left: 50%;
            transform: translateX(-50%);
            width: 80%;
            margin: 0 auto;
            padding: 2em;
            background-color: white;

            h5 {
            text-align: center;
            font-family: $fontFamily;
            padding-bottom: 1.5em;
            display: flex;
            justify-content: center;
            align-items: center;
            }

            h5::after {
                content: '';
                display: inline-block;
                width: 39%;
                height: 1px;
                background-color: $silverChalice;
                margin: 1em;
            }

            h5::before {
                content: '';
                display: inline-block;
                width: 39%;
                height: 1px;
                background-color: $silverChalice;
                margin: 1em;
            }

            ul {
            display: flex;
            justify-content: space-between;
            list-style: none;

            li {
                display: flex;
                flex-direction: column;
                justify-content: center;
                text-align: center;
                width: 29%;
                cursor: pointer;

                h4,
                p {
                width: 95%;
                padding-top: 1em;
                }

                .data {
                    font-family: $fontFamily;
                    font-size: 0.5em;
                    color: $silverChalice;
                }
            }

            li:hover .hover {
                display: block;
            }
            }
        }

        .img-jumbotron {
            position: relative;
            .hover {
                position: absolute;
                top: 50%;
                left: 50%;
                transform: translate(-50%, -50%);
                background: rgb(255,127,0);
                background: linear-gradient(350deg, rgba(255,127,0,1) 61%, rgba(255,255,255,1) 100%);
                opacity: 0.9;
                width: 101%;
                height: 101%;
                display: none;

                p {
                    position: absolute;
                    top: 50%;
                    left: 50%;
                    transform: translate(-50%, -50%);
                    color: $springWood;
                }

                .fa-link {
                    position: absolute;
                    top: 40px;
                    transform: translateX(-50%);
                    font-size: 0.7em;
                    background-color: $springWood;
                    padding: 0.5em;
                    border-radius: 50%;
                    
                }
            }
        }
        
    }

    
</style>