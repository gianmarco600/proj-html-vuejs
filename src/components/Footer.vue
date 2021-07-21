<template>
    <footer>
        <div class="container-md">
            <div class="row">
                <div class="col-6">
                    <ul>address
                        <li v-for="link in footerDatas.address" :key="link">{{link}}</li>
                    </ul>
                    <div>social</div>
                </div>
                <div class="col-6">
                    <div class="row">
                        <div class="col-4">
                            <ul>explore
                                <li v-for="link1 in footerDatas.explore1" :key="link1">link1</li>
                            </ul>
                        </div>
                        <div class="col-4">
                            <ul>
                                <li v-for="link2 in footerDatas.explore2" :key="link2">{{link2}}</li>
                            </ul>
                        </div>
                        <div class="col-4">
                            <ul>information
                                <li v-for="link3 in footerDatas.information" :key="link3">{{link3}}</li>
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
    margin-top: 70px;
    background-color: $HintOfRed;
    padding: 50px 0;
}
</style>