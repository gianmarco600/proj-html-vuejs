<template>
    <div class="holder">
        <section>
            
            <div class="sezione container-md">
                <img src="@/assets/img/home-6-services-image-1024x411.png" alt="">
                <h5>{{prefootDatas.intro}}</h5>
                <h2>{{prefootDatas.main}}<span></span></h2>
                <div class="row mt-5">
                    <div v-for="item in prefootDatas.cols" :key="item" class="col-3">
                        <div class="ico"><i :class="item.ico"></i></div>
                        <h4>{{item.main}}</h4>
                        <p>{{item.text}}</p>
                    </div>
                </div>
            </div>
        </section>
        <h4>{{prefootDatas.cta.intro}}<span></span></h4>
        <h3>{{prefootDatas.cta.main}}</h3>
        <div class="btn_space">
            <button type="button" class="btn _green_btn">Primary</button>
        </div>
            
    </div>
    
</template>

<script>
export default {
    name:'PreFoot',
    props:{
        prefootDatas: Object
    }
}
</script>

<style lang='scss' scoped>
@import '@/style/commons.scss';
@import '@/style/vars.scss';

.holder{

width: 100%;

    section{
        background: rgb(255,255,255);
        background: linear-gradient(180deg, rgba(255,255,255,1) 0%, rgba(239,241,244,1) 71%);
        height: 900px;
        width: 100%;
        
        .sezione{
            width: 100%;
            height: 100%;
            position: relative;
            .ico{
                font-size: 100px;
                padding-left: 50px;
                
            }
            img{
                position: absolute;
                bottom: -23px;
                width: 90%;
            }
            h4{
                margin-top: 30px;
                font-size: 22px;
                font-weight: 900;
                text-align: left;

            }
            h5{
                margin-top: 70px;
                font-size: 18px;
                text-align: center;
            }
            h2{
                font-size: 40px;
                font-weight: 900;
                text-align: center;
                text-transform: capitalize;
                span{
                color:$JungleGreen;
                }
            }
            i{
                font-size: 50px;
            }
        }
        
    }
    h4{
        margin-top: 100px;
        text-align: center;
        span{
            color:$JungleGreen;
        }
    
    }
    h3{
        text-align: center;
        font-size: 40px;
    }    
    .btn_space{
        text-align: center;
        width: 100%;
        ._green_btn{
            margin: 40px auto;
        }
    }
    
}
</style>