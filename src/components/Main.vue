<template>
    <main>
        <div class="_bg">
            <section class="container-md ">
                <div class="_box">
                    <h3>{{mainDatas.intro.main}} </h3>
                    <h6>/founder & CEO</h6>
                </div>
                <div class="row">
                    <div v-for="card in mainDatas.intro.cardsDatas" :key="card" class="col-3">
                        <div class="_text">{{card.num}}</div>
                        <div class="_subtext">{{card.sub}}</div>
                    </div>  
                </div>  
                <div class="section_1">
                    <div class="row">
                        <div class="col-6">
                            <!-- colonna di sinistra col le 4 card -->
                        <div class="row">
                            <div class="col-6">
                                <div class="_vertical_row special_1">
                                    <div v-for="specialCard1 in mainDatas.intro.column1CardDatas" :key="specialCard1" class="col_4">
                                        <div class="_card">
                                            <strong>{{specialCard1.label}}</strong>
                                            <p>{{specialCard1.text}}
                                            </p>
                                            <img :src="require(`@/assets/img/${specialCard1.src}`)" alt="">
                                        </div>
                                    </div>
                                </div>
                            </div>
                            <div class="col-6">
                                <div class="_vertical_row special_2">
                                    <div v-for="specialCard2 in mainDatas.intro.column2CardDatas" :key="specialCard2" class="col_4">
                                        <div class="_card">
                                            <strong>{{specialCard2.label}}</strong>
                                            <p>{{specialCard2.text}}
                                            </p>
                                            <img class="fat" :src="require(`@/assets/img/${specialCard2.src}`)" alt="">
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>

                        </div>
                        <div class="col-6">
                            <!-- colonna di destra -->
                            <div class="_vertical_row">
                                <div class="text_box_1">
                                    <h5>{{mainDatas.intro.rightBanner.intro}}</h5>
                                    <strong>{{mainDatas.intro.rightBanner.main}} <span></span></strong>
                                    <ul>
                                        <li v-for="elem in mainDatas.intro.rightBanner.list" :key="elem"><i class="fas fa-check"></i><span>{{elem}} </span></li>
                                        
                                    </ul>
                                    <button type="button" class="btn _green_btn">Primary</button>
                                </div>
                            </div>

                        </div>
                    </div>
                </div>    
            </section>
            </div>
        <Courses 
        :coursesDatas="mainDatas.courses"
        :courses="courses"/>
        <Feeds 
        :feedsDatas="mainDatas.feed"
        :clients="clients"/>
        <Blogs 
        :blogsData="mainDatas.blog"
        :blogs="blogs"/>
        <PreFoot
        :prefootDatas="mainDatas.prefoot"
        />
    </main>
</template>

<script>
import Courses from '@/components/Courses.vue'
import Feeds from '@/components/Feeds.vue'
import Blogs from '@/components/Blogs.vue'
import PreFoot from '@/components/PreFoot.vue'

export default {
    name:"Main",
    components: {
        Courses,
        Feeds,
        Blogs,
        PreFoot
    },
    props:{
        mainDatas: Object
    },
    data(){
        return{
        
        }
    }
}
</script>

<style lang="scss" scoped>
@import '@/style/commons.scss';
@import '@/style/vars.scss';

._bg{
   background-image: url('~@/assets/img/background-pattern-grid-line.png');
    background-repeat: repeat; 
}

main{
    
    
    
    section{
        padding-top:20px ;
        ._box{
            width: 100%;
            margin-bottom: 60px;
            h3{
            margin: 0 auto;
            text-align: center;
            margin-top: 250px;
            font-weight: 900;
            line-height: 40px;
            width: 60%;
            
            }
            h4{
                margin: 50px auto 5px auto;
                text-align: center;
                text-transform: uppercase;
                font-weight: 900;
                font-size: 20px;

            }
            h6{
                margin-top: 40px;
                text-align: center;
                color: rgb(185, 185, 185);
            }
        }
        ._text{
            font-size: 40px;
            color: $JungleGreen;
            font-weight: 900;
            text-align: center;
            margin: 20px 0;
        }
        ._subtext{
            text-transform: uppercase;
            font-size: 16px;
            text-align: center;
            font-weight: 900;
            color: $ShadyLady;
        }
        .section_1{
            margin-top: 50px;
            display: block;
            width: 100%;
            height: 900px;
            .row{
                height: 100%;
                .col-6{
                    height: 100%;
                    ._vertical_row{
                        display: flex;
                        flex-direction: column;
                        height: 100%;
                        width: 100%;
                        justify-content: center;
                        align-items: center;
                        .col_4{
                            height: 55%;
                            width: 100%;
                            padding: 20px 0;
                            ._card{
                                width: 80%;
                                margin: 20px auto;
                                height: 100%;
                                background-color: $White;
                                border-radius: 7px;
                                box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;
                                padding: 15px 10px;
                                
                                p{
                                    line-height: 1.2rem;
                                    font-size: 14px;
                                    margin: 10px 0;
                                }
                                img{
                                    width: 100%;
                                    bottom: 10px;
                                }
                                .fat{
                                    width: 70%;
                                    margin: 0 auto;
                                }

                                

                            }
                        }
                                                
                        .text_box_1{
                            width: 90%;
                            height: 60%;
                            padding: 30px;
                            // background-color: red;
                            h5{
                                margin:30px 0;
                                font-size: 16px;
                                text-transform: uppercase;
                                color:$ShadyLady ;
                            }
                            strong{
                                font-size: 50px;
                                text-transform: capitalize;
                                font-weight: 900;
                                span{
                                    color:$JungleGreen ;
                                }
                            }
                            ul{
                                list-style: none;
                                margin: 30px 0;
                                padding: 5px 0;
                                li{
                                    margin: 10px 0;
                                    color: $JungleGreen ;
                                    span{
                                        margin-left: 10px;
                                        color: black;
                                    }
                                    
                                }
                            }
                        }
                    }
                    .special_1{
                                height: 70%;
                                margin-top: 40px;
                            }
                    .special_2{
                        height: 70%;
                        margin-top: 120px;
                    }    
                }
            }
        }
    }
}
    
</style>