<template>
    <div class="jumbotron-tot">
        <div @mouseover="stopAutoplay" @mouseleave="startAutoplay" class="jumbotron">
            <img :src="journals[counter].img" alt="">
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
                <h1>{{ journals[counter].text }}i</h1>
                <p>{{ journals[counter].admin }}</p>
                </div>
            </div>
            <div class="foodie-journal">
                <h5>FOODIE JOURNAL</h5>
                <ul>
                    <li @click="changeImage(index)" v-for="(journal, index) in journals"
                        :key= "index">
                        <div class="img-jumbotron">
                            <img :src="journal.img" alt="">
                            <div class="hover">
                                <div class="hover-center">
                                    <i class="fas fa-link"></i>
                                    <p>{{ journal.text }}</p>
                                </div>
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
            counter: 0,
            autoPlayInterval: null,
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
    },

    methods: {
        changeImage: function(index) {
            this.counter = index;
        },
        stopAutoplay: function () {
        clearInterval(this.autoPlayInterval);
        this.autoPlayInterval = null;
        },
        startAutoplay: function () {
            this.autoPlayInterval = setInterval(() => {
            this.next();
            }, 4000);
        },
        next: function () {
        this.counter += 1;
        if (this.counter > this.journals.length - 1) {
          this.counter = 0;
        }
      },
    }
}
</script>

<style lang="scss">
@import "../assets/scss/partials/_variables.scss";

    .jumbotron-tot {
        width: 100%;
        height: 850px;
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
            width: 50%;
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

                .hover-center {
                    width: 100%;
                    height: 100%;
                    display: flex;
                    flex-direction: column;
                    justify-content: center;
                    align-items: center;


                    p {
                        color: $springWood;
                        text-align: center;
                        font-size: 0.6em;
                    }

                    .fa-link {
                        font-size: 0.7em;
                        background-color: $springWood;
                        padding: 0.5em;
                        border-radius: 50%;
                        font-size: 0.5em;
                    }
                }    

            }
        }
        
    }

    
</style>