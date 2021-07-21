<template>
    <section>
        <div class="container-md">
            <h2>{{feedsDatas.main}} <span></span></h2>
        
            <div class="paragraph">
                <div class="image">
                    <img src="@/assets/img/testimonial-avata-02.jpg" alt="">
                    <img class="effect_1" src="@/assets/img/maxcoach-shape-05-150x150.png" alt="">
                </div>
                <div class="text">
                    <p>{{feedsDatas.text}}</p>
                    <strong>Mina Hollace</strong>
                    <h6>/Freelance</h6>
                </div>
                
                
            </div>
            <div class="row">
                <div v-for='(client, i ) in feedsDatas.clients' :key="i" class="col-2 justify-content-around">
                    <img class="client" :src="require(`@/assets/img/${client}`)" alt="">
                </div>
                
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Feeds',
    props:{
        
        feedsDatas: Object
    }
}
</script>

<style lang='scss' scoped>
@import '@/style/commons.scss';
    
section{
    padding: 50px 0;
    h2{
        margin-top: 70px;
        font-size: 40px;
        font-weight: 900;
        text-align: center;
        text-transform: capitalize;
        span{
            color:$JungleGreen;
        }
    }
    .paragraph{
        width: 90%;
        margin: 100px auto;
        display: flex;
        .image{
            width: 300px;
            height: 300px;
            display: inline-block;
            position: relative;
            img{
                display: block;
                width: 200px;
                height: 200px;
                border-radius: 50%;
                position: absolute;
                top: 50%;
                left: 50%;
                transform: translate(- 50%, - 50%);
                z-index: 9999;
            }
            .effect_1{
                top: 65%;
                left: 65%;
                width: 150px;
                height: 150px;
                z-index: 999;
            }
        }
        .text{
            display: inline-block;
            width: 70%;
            padding: 25px 20px;
            p{
                font-size: 30px;
                margin: 20px 0;
            }

        }
    }
    .client{
            height: 35px;
            
            margin: 0 auto;
            display: block;
            
        
    }
}
</style>