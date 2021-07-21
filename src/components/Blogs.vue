<template>
    <section>
        <div class="container-md">
            <h5>{{blogsData.intro}}</h5>
            <h2>{{blogsData.main}}<span></span></h2>
            <div class="row card_box">
                <div v-for="blog in blogsData.cards" :key="blog" class="col-4">
                    <img :src="require(`@/assets/img/${blog.src}`)" alt="">
                    <h6>{{blog.tema}}</h6>
                    <p>{{blog.main}} </p>
                    <span class="info"><i class="far fa-calendar"></i><span>{{blog.data}}</span></span>
                    <span class="info"><i class="far fa-eye"></i><span>{{blog.views}} views</span></span>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Blogs',
    props:{
        
        blogsData: Object
    }
}
</script>

<style lang='scss' scoped >
@import '@/style/commons.scss';
@import '@/style/vars.scss';

section{
    padding: 50px 0;
    background-color: $HintOfRed;
    h5{
        margin-top: 70px;
        text-align: center;
        text-transform: uppercase;
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
    .card_box{
        height: 500px;
        width: 100%;
        padding: 10px;
        margin: 70px 0;
        p{
            font-size: 20px;
            font-weight: 700;
            transition: 0.8s;
            &:hover{
                color: $JungleGreen;
                transition: 0.3s;
                cursor: pointer;
            }
        }
        h6{
            font-weight: 200;
            font-size: 22px;
        }
        .info{
            span{
                margin-left: 5px;
                font-size: 14px;
            }
        }
        img{
            width: 95%;
            border-radius: 10px;
            margin-bottom: 20px;
        }
        span{
            margin-right: 30px;
        }
    }
    
}
</style>