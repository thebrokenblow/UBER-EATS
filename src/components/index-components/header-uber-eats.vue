<template>
  <header>
    <div class="d-flex shadow-sm justify-content-between p-4 header">
      <div>
        <a class="logo-header" href="#">
          <img src="./svg/logo.svg" alt="uber eats" />
        </a>
      </div>
      <div>
        <button type="button" class="btn btn-outline-dark button-nav">
          Войти
        </button>
        <a class="navbar-brand basket-header" href="#">
          <img class="basket" src="./svg/basket.svg" alt="basket" />
        </a>
      </div>
    </div>
  </header>
</template>

<style>
.header {
  height: 80px;
}

.logo-header {
  padding-left: 40px;
}

.basket-header {
  margin-right: 40px;
}

.basket {
  height: 30px;
  width: 30px;
}

.button-nav {
  border: 1px solid #e0e0e0;
  border-radius: 2px;
  font-weight: 500;
  margin-right: 20px;
}
</style>
