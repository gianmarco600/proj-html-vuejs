<template class="fixedmenu">
  <div class="fixedmenu">
      <ul class="menu">
        <li>
            <i class="fas fa-ruler-combined"></i>
            <div class="label" > <h6>select demo </h6> 
                  <span><i class="fas fa-arrows-alt-h"></i>
                  </span>
            </div>
        </li>
        <li>
            <i class="far fa-life-ring"></i>
            <div class="label" ><h6>support channel</h6> 
                <span><i class="fas fa-arrows-alt-h"></i>
                </span>
            </div>
        </li>
        <li>
            <i class="fas fa-book"></i>
            <div class="label" > <h6>documentation</h6> 
                <span><i class="fas fa-arrows-alt-h"></i>
                </span>
            </div>
        </li>
        <li>
            <i class="fas fa-shopping-cart"></i>
            <div class="label" ><h6>purchase maxcoach</h6> 
                <span><i class="fas fa-arrows-alt-h"></i>
                </span>
            </div>
        </li>
      </ul>
        
  </div>
</template>

<script>
export default {
    name:'FixedMenu'
}
</script>

<style lang="scss" scoped>
@import '@/style/commons.scss';
@import '@/style/vars.scss';
.fixedmenu{
    position: fixed;
    right: 0;
    top: 200px;
    height: 200px;
    width: 40px;
    background-color: $White;
    border-top-left-radius: 6px;
    border-bottom-left-radius: 6px;
    .menu{
        display: flex;
        flex-direction: column;
        height: 100%;
        align-items: center;
        list-style: none;
        padding: 0 5px;
        li{
            height: 25%;
            font-size: 20px;
            padding-top: 7px;
            position: relative;
            &:hover{
                cursor: pointer;
                }
            
            i{
                height: 100%;
                
            }
            .label{
                position: absolute;
                left:-30px;
                top:49%;
                width: 0;
                height: 40px;
                background-color: black;
                border-radius: 10px;
                transform: translate(-100% , -50%);
                transition:  0.2s;
                color: rgba(255, 255, 255, 0);
                text-align: center;
                padding-top: 9px;
                opacity: 0;
                font-size: 11px;
                font-weight: 700;
                text-transform: uppercase;
                h6{
                    opacity:0;
                    transition:0.1s;
                    display: inline-block;
                    color: white;
                    padding: 0 5px;
                }
                span{
                    position: absolute;
                    right: 0;
                    transform: translate(5px , 0);
                    color: black;
                    font-size: 20px;
                    opacity: 0;
                    transition: 0.1s;
                }
            }
            &:hover .label{
                opacity: 1;
                color: white;
                width: 200px;
                max-width: 200px;
                transition: 0.4s;
                
            }
            &:hover span{
                opacity: 1;
                transition: 0.5s;
            }
            &:hover h6{
                opacity: 1;
                transition: ease-in-out 0.4s;
                color: white;
                transition-delay: 0.2s;
            }
        }
    }
}
</style>