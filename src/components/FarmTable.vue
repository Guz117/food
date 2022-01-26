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

                <div class="load-more">
                    <p>LOAD MORE POSTS</p>
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
            <div class="singapore">
                <div class="singapore-img">
                    <img :src="require('../assets/images/singapore-featured-image-1200x790.jpg')" alt="">
                    <h4>City Guide: Singapore</h4>
                </div>
                <div class="all-city">
                    <p><i class="fas fa-globe-americas"></i><a href="#"> VIEW ALL CITY GUIDES</a> </p>
                </div>
            </div>

            <div class="search">
                <i class="fas fa-search"></i>
                <label for="search">Search...</label>
                <input id="search" type="text" placeholder="Search...">
            </div>

            <div class="follow">
                <p>Follow Us</p>
                <ul>
                    <li><a href="#"><i class="fab fa-facebook-f"></i></a></li>
                    <li><a href="#"><i class="fab fa-instagram"></i></a></li>
                    <li><a href="#"><i class="fab fa-twitter"></i></a></li>
                    <li><a href="#"><i class="fab fa-youtube"></i></a></li>
                    <li><a href="#"><i class="fab fa-pinterest-p"></i></a></li>
                </ul>
            </div>
            <div class="buttons">
                <span id="popular">Popular</span><span>Recent</span>
            </div>
            <div class="popular">
                <ul class="ul-popular">
                    <li class="li-popular" v-for="(popular, index) in populars"
                        :key= "index">
                        <div class="img-popular">
                            <img :src="popular.img" alt="">
                        </div>
                        <div class="text-popular">
                            <p class="title-popular">{{ popular.title }}<p/>
                            <p class="data-popular">{{ popular.subTitle }}</p>
                        </div>
                    </li>        
                </ul>
            </div>
            <div class="tweet">
                <div class="theme">
                    <p><span id="span-tweet">Tweets</span> <span id="by">by</span> <a href="#" class="fusion">@Theme_Fusion</a></p>
                    <div class="info">
                        <img :src="require('../assets/images/image.svg')" alt="">
                    </div>
                </div>
                <div class="center-tweet">
                    <div class="tweet-left">
                        <img :src="require('../assets/images/3a74ce3d0532b7773b174c45ca3bd05a_normal.png')" alt="">
                    </div>
                    <div class="tweet-right">
                        <div class="fusion-title">
                            <p>ThemeFusion</p>
                            <img :src="require('../assets/images/image (1).svg')" alt="">
                        </div>
                        <p class="fusion">@Theme_Fusion</p>
                        <p class="need">Do you need sublime WordPress hosting for your next website? Take advantage of exclusive partner offers that we have secured just for you, &amp; launch your site in second with <a href="#">&#35;avada</a> on WP Engine Hosting &amp; get 30% Off this BlackFriday <a href="#">bit.ly/kjLLE2 &#35;BlackFriday 2020</a></p>
                        <div class="black-friday">
                            <img :src="require('../assets/images/En2TRxLW4AEiWUN.jpeg')" alt="">
                        </div>
                        <div class="icon">
                            <div class="icon-img">
                                <img :src="require('../assets/images/image (2).svg')" alt="">
                                <img :src="require('../assets/images/image (3).svg')" alt="">
                            </div>
                            <p>21h</p>
                        </div>
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
            populars: [
                {
                    img: require('../assets/images/single-post-img3-66x66.jpg'),
                    title: 'Food Corner: Top Japanese restaurant for Sushi',
                    subTitle: 'March 25th 2019',
                },
                {
                    img: require('../assets/images/slide1-bg-66x66.jpg'),
                    title: 'City Guide: Singapore',
                    subTitle: 'February 27th 2019',
                },
                {
                    img: require('../assets/images/single-post-img3-66x66.jpg'),
                    title: '6 Nutritional Tips to Help Burn Body Fat',
                    subTitle: 'February 28th 2019',
                },
            ],
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
    padding: 5em 0;
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

        .load-more {
            width: 100%;
            margin-top: 1em;
            background-color: $osloGray;
            cursor: pointer;
            p {
                color: $capeCod;
                font-family: $fontFamily;
                font-size: 0.8em;
                text-align: center;
            }
        }
    }

    



    
    .col-right {
        width: 30%;
        height: 100%;


        .recipes {
            width: 100%;
            position: relative;
            
            img {
                width: 100%;
                height: 100%;
                object-fit: cover;
            }

            .recipes-text {
                position: absolute;
                top: 50%;
                left: 50%;
                transform: translate(-50%, -50%);
                text-align: center;
                font-family: $fontFamily;
                font-size: 0.7em;
            }
        }

        .singapore {
            width: 100%;
            padding-top: 2em;

            

            .singapore-img {
                position: relative;
                img {
                width: 100%;
                }
            }
            h4 {
                position: absolute;
                bottom: 2em;
                font-size: 0.7em;
                color: white;
                background-color: rgba(0, 0, 0, 0.5);
                padding: 2px 5px;
            }
            .all-city {
                width: 100%;
                background-color: $orange;
                font-size: 0.6em;
                text-align: center;
                padding: 5px 0;
                font-family: $fontFamily;
                color: white;

                a {
                    color: white;
                    text-decoration: none;
                }
            }
            
        }

        .singapore::after {
                content: "";
                display: inline-block;
                width: 100%;
                height: 0.5px;
                background-color: #afafaf;
        }

        .search {
            margin-top: 2em;
            width: 1.6em;
            height: 1.6em;
            border-radius: 5px;
            background-color: white;
            font-size: 1em;
            color: $silverChalice;
            border: 1px solid $silverChalice;
            }
            .search {
            display: flex;
            align-items: center;
            justify-content: space-around;
            width: 100%;
            height: 1.6em;
            border-radius: 5px;
            background-color: white;
            }
            .search:focus-within {
            border: 2px solid $orange;
            }
            .search:focus-within i {
            color: $orange;
            }
            .search label {
            display: none;
            }
            .search input {
            width: 85%;
            background-color: transparent;
            border: 0;
            outline: 0;
            }

            .follow {
                margin-top: 2em;
                p {
                    color: $orange;
                    font-size: 0.8em;
                    padding-bottom: 0.5em;
                }
                ul {
                    display: flex;
                    list-style: none;

                    li {
                        width: 20px;
                        height: 20px;
                        display: flex;
                        justify-content: center;
                        align-items: center;
                        margin: 0 0.1em;
                        background-color: $silverChalice;
                        border-radius: 2px;
                        

                        a {
                            padding: 0.2em;
                            color: $nevada;
                        }
                    }
                }
            }

            .buttons {
                margin-top: 2em;
                display: flex;
                justify-content: center;


                span {
                    padding: 0 1em;
                    background-color: $cararra;
                    border: 0;
                    color: $capeCod;
                    font-size: 0.9em;
                    border: 0.3px solid $nevada;
                    cursor: pointer;
                }

                span:hover {
                    background-color: white;
                }
            }

            .popular {
                margin-top: 2em;
                .ul-popular {
                list-style: none;

                .li-popular {
                    display: flex;
                    align-items: center;
                    padding-bottom: 0.5em;


                    img {
                        width: 40px;
                        height: 40px;
                        border-radius: 50%;
                    }

                    .text-popular {
                        padding-left: 0.5em;

                        .title-popular {
                            font-size: 0.5em;
                            font-family: $fontFamily;
                        }
                        .data-popular {
                            font-size: 0.4em;
                            font-family: $fontFamily;
                            color: $nevada;
                        }
                    }
                }
            }
            }

            .tweet {
                width: 100%;
                padding: 0.5em;
                background-color: white;
                font-family: $fontFamily;

                .theme {
                    width: 100%;
                    display: flex;
                    align-items: center;
                    justify-content: space-between;
                    p {
                        font-size: 0.7em;
                        #by {
                            font-size: 0.3em;
                            color: $nevada;
                        }
                        a {
                            text-decoration: none;
                            font-size: 0.6em;
                        }
                    }
                    .info {
                        img {
                            width: 10px;
                        }
                    }
                }

                .center-tweet {
                    width: 95%;
                    height: 90%;
                    margin: 0 auto;
                    display: flex;
                    .tweet-left {
                        width: 10%;
                        img {
                            width: 100%;
                        }
                    }
                    .tweet-right {
                        width: 100%;
                        height: 100%;
                        .fusion-title {
                            width: 100%;
                            display: flex;
                            justify-content: space-between;
                            align-items: center;
                            p {
                                font-size: 0.6em;
                            }
                            
                            img {
                                width: 7%;
                                }
                            
                        }
                        .fusion {
                            font-size: 0.4em;
                            color: $nevada;
                        }

                        .need {
                            font-size: 0.5em;
                            a {
                                text-decoration: none;
                            }
                        }

                        .black-friday {
                            width: 100%;
                            margin: 0 auto;
                            padding-top: 1em;
                            img {
                                width: 100%;
                            }
                        }

                        .icon {
                            display: flex;
                            align-items: center;
                            justify-content: space-between;
                            .icon-img {
                                img {
                                    width: 12px;
                                    padding-right: 5px;
                                }
                            }
                            p {
                                font-size: 0.5em;
                            }
                        }
                    }
                }

                
            }
            

    }
}
</style>