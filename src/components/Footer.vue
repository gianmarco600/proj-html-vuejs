<template>
    <footer>
        <div class="container-md">
            <div class="row">
                <div class="col-6">
                    <ul>address
                        <li v-for="link in footerDatas.address" :key="link"><a href="#">{{link}}</a></li>
                    </ul>
                    <div>
                        <a class="social" href="#"><i class="fab fa-facebook-square"></i></a>
                        <a class="social" href="#"><i class="fab fa-twitter-square"></i></a>
                        <a class="social" href="#"><i class="fab fa-instagram"></i></a>
                        <a class="social" href="#"><i class="fab fa-linkedin"></i></a>
                    </div>
                </div>
                <div class="col-6">
                    <div class="row">
                        <div class="col-4">
                            <ul>explore
                                <li v-for="link1 in footerDatas.explore1" :key="link1"><a href="#">{{link1}}</a></li>
                            </ul>
                        </div>
                        <div class="col-4">
                            <ul>
                                <li v-for="link2 in footerDatas.explore2" :key="link2"><a href="">{{link2}}</a></li>
                            </ul>
                        </div>
                        <div class="col-4">
                            <ul>information
                                <li v-for="link3 in footerDatas.information" :key="link3"><a href="">{{link3}}</a></li>
                            </ul>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name:"Footer",
    props:{
        footerDatas: Object
    }
}
</script>

<style lang="scss" scoped>
@import '@/style/commons.scss';
@import '@/style/vars.scss';


footer{
    height: 400px;
    margin-top: 100px;
    background-color: $HintOfRed;
    padding: 80px 0;
    ul{
        list-style: none;
        font-size: 20px;
        font-weight: 500;
        text-transform: capitalize;
        li{
            margin: 15px 7px;
            font-size: 16px;
            font-weight: 300;
            a{
                color: black;
                &:hover{
                    text-decoration: none;
                    color: $JungleGreen;
                }
            }
            
        }
    }
    .social{
                margin: 0 20px;
                font-size: 30px;
                color: $Silver;
            }
}
</style>