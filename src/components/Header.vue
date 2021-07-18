<template>
  <header>
    <div class="_box container-md">
      <ul class="_row justify-content-between align-items-center">
        <li class="_col">
          <!-- logo -->
          <img id="logo" src="@/assets/img/light-logo.png" alt="">
        </li>


        <li class="_col_links">
          <!-- links -->
          <ul class="links_box _row justify-content-around align-items-center">
            <li v-for="link in links" :key="link" class="link_item">
              <a href="">{{link}} <i class="fas fa-chevron-down"></i><div class="line"></div></a>
            </li>
          </ul>
        </li>


        <li class="_col">
          <!-- parte destra -->
          <ul class="_row justify-content-around align-items-center">
            <li class="search_item search_ico"><i class=" fas fa-shopping-cart"></i></li>
            <li class="search_item search_ico"><i class=" far fa-user-circle"></i></li>
            <li class="search_item _grow"><input placeholder="Search.." class="search" type="text" name="" id=""></li>
          </ul>

        </li>
      </ul>
      
    </div>
  </header>

</template>

<script>

export default {
  name: 'Header',
props:{
  links: Array
  },
  data(){
    return{
      semaforo : 0
    }
  },
  methods:{

  }

}
</script>


<style lang="scss" scoped>
@import '@/style/commons.scss';
@import '@/style/vars.scss';

header{
  width: 100%;
  height: 100px;
  background-color:$PortGore ;
  ._box{
    height: 100%;
    // background-color: red;
  }
  ._row{
    display: flex;
    width: 100%;
    height: 100%;
    padding: 10px 0;
    ._col{
      flex-basis: 20%;
      flex-grow: 0;
      // stile li laterali della navbar
      #logo{
        margin: auto;
        
        width: 90%;
      }
      .search_ico{
          flex-basis: 20px;
          font-size: 25px;
          line-height: 70px;
          margin-right: 10px;
          color: $White;
          transform: translate(0 , - 5px);
          i{
            margin: 0 10px 7px;
            
          }
        }
      .search_item{
        
        height: 100%;
        // background-color: violet;
        text-align: center;
        
        
        .search{
          width: 85%;
          margin: 0 auto;
          height: 70%;
          border: none;
          border-radius: 10px;
          padding: 3px 10px;
          transform: translate(0 , - 4px);
        }
      }
      ._grow{
          flex-grow: 1;
        }
    }
    li{
      list-style: none;
      // background-color: royalblue;
      display: inline-block;
      height: 100%;
      line-height: 70px;
    }
    ._col_links{
      flex-basis: 58%;
      flex-grow: 0;
      // stile colonna centrale della navbar
      .links_box{
        list-style: none;
        .link_item{
          flex-basis: 15%;
          flex-grow: 1;
          display: block;
          font-size: 18px;
          color: $White;
          height: auto;
          position: relative;
          .line{
              width: 0;
              height: 1px;
              background-color: $White;
              position: absolute;
              bottom: 10px;
              transition: 0.3s;
              right: 10px;
            }
            &:hover .line{
              width: 75%;
              left:10px;
              transition: 0.5s;
              
            }
          a{
            text-align: center;
            color: $White;
            text-transform: capitalize;
            text-overflow: none;
            margin: 0 auto;
            display: inline-block;
            width: 100%;
            &:hover{
              text-decoration: none;
            }
          }
        }
      }
      
    }
  }
}

</style>
