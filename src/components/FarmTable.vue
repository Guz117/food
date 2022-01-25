<template>
    <div class="farm-table">
        <div class="blog">
            <div class="blog-left">
                <h5>FARM TO TABLE</h5>
                <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Doloremque dolorum veritatis reiciendis dolor laborum voluptas</p>
            </div>
            <div class="blog-right">
                <button>READ OUR BLOG<i class="fas fa-book-reader"></i></button>
            </div>
        </div>
        <div class="col">
            <div class="col-left">
                <div class="col-left-top">
                    <div class="img">
                        <img :src="sushi[0].img" alt="">
                    </div>
                    <div class="text">
                        <div class="cont-text">
                            <h5 class="recepies-title">{{ sushi[0].title }}</h5>
                            <p class="sub-title">{{ sushi[0].subTitle }}</p>
                            <p class="text-string">{{ sushi[0].text }}</p>
                            <div class="read-more">
                                <a href="#">Read More<i class="fas fa-chevron-right"></i></a>
                                <i class="far fa-comments">o</i>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col-left-down">
                    <ul>
                        <li v-for="(farm, index) in farms"
                        :key= "index">
                            <div class="img">
                                <img :src="farm.img" alt="">
                            </div>
                            <div class="text">
                                <h4>{{ farm.title }}</h4>
                                <p class="data">{{ farm.subTitle }}</p>
                            </div>
                        </li>
                        
                        
                    </ul>
                </div>
            </div>
        
        <div class="col-right">
            <div class="recipes">
                <img :src="require('../assets/images/ad-bg.jpg')" alt="">
                <div class="recipes-text">
                    <div class="recipes-text-center">
                        <h2>VIEW OUR LATEST RECIPES</h2>
                    </div>
                </div>
            </div>

        </div>
      </div>
      
      

  </div>
</template>

<script>
export default {
    name: 'FarmTable',
    data() {
        return {
            sushi:[
                {
                    img: require('../assets/images/single-post-img3-1200x790.jpg'),
                    title: 'Food Corner: Top Japanese restaurant for Sushi',
                    subTitle: 'By Admin | March 25th 2019',
                    text: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Officiis explicabo fuga dolorem quos inventore dignissimos, architecto, porro, iste veniam maxime assumenda facere libero unde quo culpa a! Explicabo, error quo.Lorem ipsum dolor, sit amet consectetur adipisicing elit. Officiis explicabo fuga dolorem quos inventore dignissimos, architecto, porro, iste veniam maxime assumenda facere libero unde quo culpa a! Explicabo, error quo.' 
                },
            ],
            farms: [
                {
                    img: require('../assets/images/fi-roundup-1200x790.jpg'),
                    title: 'Roundup: My New Favourite Recipes For Heathy Living',
                    subTitle: 'By Admin | March 25th 2019',
                    text: 'lorem' 
                },
                {
                    img: require('../assets/images/fi-korean-food-1200x790.jpg'),
                    title: 'Why These Toast with Tea Are My New Favourite',
                    subTitle: 'By Admin | March 25th 2019',
                    text: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Officiis explicabo fuga dolorem quos inventore dignissimos, architecto, porro, iste veniam maxime assumenda facere libero unde quo culpa a! Explicabo, error quo.Lorem ipsum dolor, sit amet consectetur adipisicing elit. Officiis explicabo fuga dolorem quos inventore dignissimos, architecto, porro, iste veniam maxime assumenda facere libero unde quo culpa a! Explicabo, error quo.' 
                },
                {
                    img: require('../assets/images/fi-toasts-1200x790.jpg'),
                    title: 'Why These Toast with Tea Are My New Favourite',
                    subTitle: 'By Admin | March 25th 2019',
                    text: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Officiis explicabo fuga dolorem quos inventore dignissimos, architecto, porro, iste veniam maxime assumenda facere libero unde quo culpa a! Explicabo, error quo.Lorem ipsum dolor, sit amet consectetur adipisicing elit. Officiis explicabo fuga dolorem quos inventore dignissimos, architecto, porro, iste veniam maxime assumenda facere libero unde quo culpa a! Explicabo, error quo.' 
                },
                {
                    img: require('../assets/images/fi-street-food-1200x790.jpg'),
                    title: 'Why These Toast with Tea Are My New Favourite',
                    subTitle: 'By Admin | March 25th 2019',
                    text: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Officiis explicabo fuga dolorem quos inventore dignissimos, architecto, porro, iste veniam maxime assumenda facere libero unde quo culpa a! Explicabo, error quo.Lorem ipsum dolor, sit amet consectetur adipisicing elit. Officiis explicabo fuga dolorem quos inventore dignissimos, architecto, porro, iste veniam maxime assumenda facere libero unde quo culpa a! Explicabo, error quo.' 
                },
                {
                    img: require('../assets/images/fi-organic-breakfast-1200x790.jpg'),
                    title: 'Why These Toast with Tea Are My New Favourite',
                    subTitle: 'By Admin | March 25th 2019',
                    text: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Officiis explicabo fuga dolorem quos inventore dignissimos, architecto, porro, iste veniam maxime assumenda facere libero unde quo culpa a! Explicabo, error quo.Lorem ipsum dolor, sit amet consectetur adipisicing elit. Officiis explicabo fuga dolorem quos inventore dignissimos, architecto, porro, iste veniam maxime assumenda facere libero unde quo culpa a! Explicabo, error quo.' 
                },
                {
                    img: require('../assets/images/fi-water-side-rest-1200x790.jpg'),
                    title: 'Why These Toast with Tea Are My New Favourite',
                    subTitle: 'By Admin | March 25th 2019',
                    text: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Officiis explicabo fuga dolorem quos inventore dignissimos, architecto, porro, iste veniam maxime assumenda facere libero unde quo culpa a! Explicabo, error quo.Lorem ipsum dolor, sit amet consectetur adipisicing elit. Officiis explicabo fuga dolorem quos inventore dignissimos, architecto, porro, iste veniam maxime assumenda facere libero unde quo culpa a! Explicabo, error quo.' 
                },
            ],
        }
    }
}
</script>

<style lang="scss">
@import "../assets/scss/partials/_variables.scss";

.farm-table {
    background-color: $cararra;
    margin: 0 auto;
    padding-top: 5em;
}

.blog {
    width: 80%;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.blog-left {
    width: 50%;
    font-family: $fontFamily;
    p {
        font-size: 0.7em;
        padding-top: 1em;
        line-height: 2em;
    }
}

.blog-right {
    button {
        color: $springWood;
        background-color: $orange;
        padding: 0.5em;
        border: 0;
        font-size: 0.7em;
        margin-top: 2em;
        .fa-book-reader {
            padding-left: 10px;
        }
    }
}

.col {
    width: 80%;
    height: 1500px;
    margin: 0 auto;
    margin-top: 2em;
    display: flex;
    justify-content: space-between;
    

    .col-left {
        width: 65%;
        height: 100%;
        

        .col-left-top {
            width: 100%;
            background-color: white;

            .img {
            width: 100%;
            position: relative;
                img {
                    width: 100%;
                    object-fit: cover;
                }
            }

            .cont-text {
                width: 90%;
                margin: 0 auto;
                padding-bottom: 1em;
                
                .recepies-title {
                font-size: 1.2em;
                }

                p {
                    font-family: $fontFamily;
                    font-size: 0.7em;
                }

                .sub-title {
                    padding-top: 1em;
                }
                .sub-title::after {
                    content: '';
                    display: inline-block;
                    width: 90%;
                    height: 1px;
                    background-color: $silverChalice;
                    margin: 1em;
                }

                .text-string {
                    padding-top: 1em;
                }

                .read-more {
                    padding-top: 1em;
                    display: flex;
                    align-items: center;
                    justify-content: space-between;

                    a {
                        text-decoration: none;
                        font-family: $fontFamily;
                        color: $shark;
                        font-size: 0.6em;
                    }

                    .fa-chevron-right {
                        font-size: 0.6em;
                        padding-left: 3px;
                    }

                    .fa-comments {
                        font-size: 0.7em;
                    }
                }
            }
        }


        .col-left-down {
            width: 100%;
            
            margin-top: 1em;
            

            ul {
                list-style: none;
                display: flex;
                flex-wrap: wrap;
                gap: 5px;
                justify-content: space-between;
            }
            li {
                width: 48%;
                background-color: white;

                .img {
                    width: 100%;
                
                    img {
                        width: 100%;
                    }
                }

                .text {
                    width: 95%;
                    display: flex;
                    flex-direction: column;
                    text-align: center;
                    font-size: 0.8em;

                    p{
                        font-family: $fontFamily;
                        font-size: 0.7em;
                        padding-top: 0.5em;
                    }
                }
            }
        }
    }

    



    
    .col-right {
        width: 29%;
        height: 100%;
        background-color:blueviolet;

        .recipes {
            width: 100%;
            height: 250px;
            position: relative;
            background-color: yellow;
            img {
                width: 100%;
                height: 100%;
                object-fit: cover;
            }

            .recipes-text {
                position: absolute;
                top: 0;
                
                .recipes-text-center {
                    width: 100%;
                    height: 100%;
                    display: flex;
                    justify-content: center;
                    align-items: center;
                }
            }
        }
    }
}
</style>