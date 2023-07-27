<template>
  <header>
    <div class="d-flex shadow-sm justify-content-between p-4 header">
      <div>
        <a class="logo-header" href="#">
          <img src="./svg/uber-eats-logo1.svg" alt="uber eats" />
        </a>
      </div>
      <div>
        <button type="button" class="button-header btn btn-outline-dark">
          Войти
        </button>
        <a class="basket-header" href="#">
          <img class="basket" src="./svg/basket-logo.svg" alt="basket" />
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
  padding-left: 80px;
}

.basket-header {
  padding-right: 80px;
}

.basket {
  height: 30px;
  width: 30px;
}

.button-header {
  border-radius: 2px !important;
  margin-right: 20px;
}
</style>
