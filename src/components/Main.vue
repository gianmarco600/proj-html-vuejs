<template>
    <main>
        <section class="container-md ">
            <div class="_box">
                <h3>Lorem ipsum dolor sit amet consectetur adipisicing elit. Beatae natus itaque dolore ut facere enim laboriosam ea exercitationem omnis, nesciunt placeat ullam.</h3>
                <h4>fannie moreno</h4>
                <h6>/founder & CEO</h6>
            </div>
            <div class="row">
                <div class="col-3">
                    <div class="_text">1.926</div>
                    <div class="_subtext">finished sessions</div>
                </div>  
                <div class="col-3">
                    <div class="_text">1.926</div>
                    <div class="_subtext">finished sessions</div>
                </div>   
                <div class="col-3">
                    <div class="_text">1.926</div>
                    <div class="_subtext">finished sessions</div>
                </div>
                <div class="col-3">
                    <div class="_text">1.926</div>
                    <div class="_subtext">finished sessions</div>
                </div>
            </div>  
            <div class="section_1">
                <div class="row">
                    <div class="col-6">
                        <!-- colonna di sinistra col le 4 card -->


                    </div>
                    <div class="col-6">
                        <!-- colonna di destra -->
                        <div class="_vertical_row">
                            <div class="text_box_1">
                                <h5>together we can create</h5>
                                <strong>service we <span>can provide</span> for my clients.</strong>
                                <ul>
                                    <li><i class="fas fa-check"></i><span> Lorem ipsum dolor sit amet consectetur </span></li>
                                    <li><i class="fas fa-check"></i><span> Lorem ipsum dolor sit amet consectetur </span></li>
                                    <li><i class="fas fa-check"></i><span> Lorem ipsum dolor sit amet consectetur </span></li>
                                    <li><i class="fas fa-check"></i><span> Lorem ipsum dolor sit amet consectetur </span></li>
                                </ul>
                                <button type="button" class="btn _green_btn">Primary</button>
                            </div>
                        </div>

                    </div>
                </div>
            </div>    
        </section>
    </main>
</template>

<script>
export default {
    name:"Main",
    data(){
        return{
            
        }
    }
}
</script>

<style lang="scss" scoped>
@import '@/style/commons.scss';
@import '@/style/vars.scss';


main{
    background-image: url('~@/assets/img/background-pattern-grid-line.png');
    background-repeat: repeat;
    
    
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
                }
            }
        }
    }
}
    
</style>