<template>
    <section>
        <div class="container-md">
            <h4>{{coursesDatas.intro}}</h4>
            <h3>{{coursesDatas.main}}<span></span></h3>
            <div class="courses row justify-content-between">
                <div v-for="course in coursesDatas.coursesList" :key="course" class="_col">
                    <div class="_card">
                        <div class="info">
                            <div class="rounded_img" >
                                <img :src="require(`@/assets/img/${course.src}`)" alt="">
                            </div>
                            <div class="text_info">
                                <div class="prezzo">{{course.price}}</div>
                                <div class="des">{{course.descr}}</div>
                                <span class="sub lessons"><i class="far fa-sticky-note"></i><span>{{course.lessons}} lessons</span></span>
                                <span class="sub students"><i class="far fa-user"></i><span>{{course.students}} students </span></span>
                            </div>
                        </div>
                    </div>
                </div>
                
            </div>
            <button type="button" class="btn _green_btn">Primary</button>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Courses',
    props:{
        courses:Array,
        coursesDatas: Object
    },
    data(){
        return{
            
        }
    }
}
</script>

<style lang="scss" scoped>
@import '@/style/commons.scss';

section{
    background-color: $HintOfRed;
    padding-top: 80px;
    height: 1100px;
    .container-md{
        height: 900px;
        text-align: center;
        ._green_btn{
            margin: 570px auto;
            // position: relative;
            // top: 400px;
        }
    
    
        h4{
            text-align: center;
            font-size: 18px;
            margin-top: 70px;
        }
        h3{
            text-align: center;
            font-size: 50px;
            font-weight: 900;
            text-transform: capitalize;
            span{
                color: $JungleGreen;
            }
        }
        ._col{
            width: 49%;
            height: 200px;
            margin: 20px 0;
        }
        .courses{
            flex-wrap: wrap;
            padding: 20px 10px;
            height: 200px;
            margin: 20px 0;
            ._card{
                width: 100%;
                height: 200px;
                // background-color: red;
                .info{
                    display: flex;
                    height: 100%;
                    width: 100%;
                    padding: 20px 20px;
                    justify-content: space-between;
                    border-radius: 10px;
                    &:hover{
                        background-color: $White;
                        transition: .5s;
                        box-shadow: rgba(149, 157, 165, 0.2) 0px 8px 24px;
                    }
                
                    .rounded_img{
                        width: 32%;
                        height: 100%;
                        // background-image: url('~@/assets/img/course-02-480x298.jpg');
                        background-position: center;
                        border-radius: 50%;
                        
                        img{
                            border-radius: 50%;
                            width: 100%;
                            height: 100%;
                            
                            
                        }
                    }
                    .text_info{
                        width: 67%;
                        height: 100%;
                        padding: 10px 20px;
                        text-align: left;
                        .prezzo{
                            font-size:25px;
                            font-weight: 900;
                            color: $JungleGreen;
                        }
                        .des{
                            font-size:21px;
                            font-weight: 700;
                            margin: 10px 0;
                        }
                        .sub{
                            font-size:14px;
                            font-weight: 900;
                            color: $Silver;
                            margin-right: 20px;
                            margin-top: 10px;
                            span{
                                margin-left: 5px;
                            }
                        }
                    }
                }    
            }
        }
    }
}
</style>