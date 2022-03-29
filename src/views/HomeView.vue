<template>
  <div class="home">
    <div class="header">
   <h2 class="title">Hi <b>Vadin!</b></h2>
      <div class="input">
        <input type="text" placeholder="find what you want...." />
        <div class="icon-input">
          <i class="bx bx-search-alt"></i>
        </div>
      </div>
      <div class="combo-header">
        <div class="text">
          <h3>Free Combo</h3>
          <p>Burguer + Coca-cola for new user</p>
        </div>
        <div class="img">
          <img
            src="https://w7.pngwing.com/pngs/573/126/png-transparent-whopper-hamburger-cheeseburger-chile-con-queso-big-king-burguer-combo-thumbnail.png"
            alt=""
          />
        </div>
      </div>
    </div>
    <div class="scroll-menu">
      <div class="scroll-content">
        <div :key="index" class="avatar" v-for="(item, index) in 10">
          <i class="bx bxs-pizza bx-sm"></i>
        </div>
      </div>
    </div>
    <h2>Top Products</h2>
    <div class="scroll-menu">
      <div class="scroll-content">
        <div :key="index" v-for="(item, index) in 10" class="top-products">
      <div class="top-products-img">
        <img width="100px" src="https://images.unsplash.com/photo-1568909344668-6f14a07b56a0?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MXx8anVpY2V8ZW58MHx8MHx8&auto=format&fit=crop&w=500&q=60" alt="" />
      </div>

        <div class="top-products-text">
          <div class="top-products-title">berry juice</div>
          <div class="top-prodcuts-price">$7.5</div>
        <i class="bx bx-plus-medical"></i>

      </div>
    </div>
      </div> 
    </div>
  </div>
</template>

<style lang="less">
h2 {
  font-weight: 300;
  margin-top: 2px;
}
.home {
  .scroll-menu {
    .scroll-content {
      display: flex;
      overflow-y: auto;
      &::-webkit-scrollbar {
        display: none;
      }
    }
  }
  .top-products {
    .top-products-img {
      margin-top: 5px;
      img {
        width: 100%;
        border-radius: 10px;
      }
    }
    i {
      position: absolute;
      right: 0;
      bottom: 0;
      padding: 10px;
      color: white;
      border-radius: 50px;
      background-color: green;
      margin: 5px;
    }
    padding: 5px;
    border-radius: 10px;
    min-width: 150px;
    position: relative;
    .top-products-text {
        margin-top: 10px;
        color: rgba(255, 131, 62);
      .top-products-title {
        color: rgba(47, 47, 47);
      }
    }
  }
  margin: 30px;
  .scroll-menu {
    margin-top: 15px;
    .scroll-content {
      display: flex;
      overflow-y: auto; //para que no se salga del contendoer el scroll
      .avatar {
        background-color: rgba(250, 248, 248);
        padding: 20px;
        border-radius: 10px;
        margin: 5px;
        i {
          color: #bf9072;
        }
      }
    }
  }
}
.header {
  .combo-header {
    background-color: #48a052;
    color: white;
    padding: 10px;
    border-radius: 10px;
    display: flex;
    align-items: center;
    margin-top: 5px;
    .img {
      width: 50%;
      img {
        width: 100%;
        object-fit: cover;
        border-radius: 10px;
      }
      width: 50%;
      object-fit: cover;
      
    }
    .text {
      width: 50%;
      h3 {
        font-weight: 400; //transparencia del texto
      }
      p {
        font-weight: 300;
      }
    }
  }
  .input {
    display: flex; //alinear objetos horizontalmente
    position: relative;
    align-items: center; //centrar horizontal los elementos
    margin-top: 5px; //para bajar el objeto
    input {
      width: 100%;
      background-color: rgba(250, 248, 248);
      border: none;
      outline: none;
      padding: 10px;
      padding-left: 30px; //correr objeto de la izquierda
      border-radius: 10px;
    }
    .icon-input {
      position: absolute;
      margin-left: 10px;
    }
  }
  .title {
    font-weight: 350;
  }
}
</style>





