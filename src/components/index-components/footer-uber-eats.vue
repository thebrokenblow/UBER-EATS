<template>
  <footer class="footer-uber-eats">
    <div class="footer-container">
      <div class="footer-logo">
        <img src="./svg/uber-eats-logo2.svg" alt="uber eats" />
      </div>
      <div class="footer-contacts-section border-top border-bottom">
        <section class="d-flex footer-contacts-container row">
          <div class="col-lg-3 col-md-4 col-12">
            <div class="dropdown">
              <button
                class="language-dropdown btn btn-secondary dropdown-toggle"
                type="button"
                id="dropdownMenuButton1"
                data-bs-toggle="dropdown"
                aria-expanded="false"
              >
                Русский
              </button>
            </div>
            <div class="name-restaurant-container">
              <span class="hashtag-restaurant">#</span>
              <span class="label-restaurant">UberEats</span>
            </div>
            <div class="d-flex social-networks-container">
              <a href="/">
                <img
                  class="icon-social-networks"
                  src="./svg/icon/facebook.svg"
                  alt="facebook"
                />
              </a>
              <a href="/">
                <img
                  class="icon-social-networks social-media-indentation"
                  src="./svg/icon/twitter.svg"
                  alt="twitter"
                />
              </a>
              <a href="/">
                <img
                  class="icon-social-networks social-media-indentation"
                  src="./svg/icon/instagram.svg"
                  alt="instagram"
                />
              </a>
            </div>
          </div>
          <div class="col-lg-3 col-md-4 col-12 row">
            <ul
              class="contacts-section second-contacts-section list-link-footer"
            >
              <li>
                <a class="text-light text-decoration-none" href="/"
                  >Об UberEats</a
                >
              </li>
              <li class="second-smaller-element-list">
                <a class="text-light text-decoration-none" href="/"
                  >Станьте партнёром по доставке</a
                >
              </li>
              <li class="second-smaller-element-list">
                <a class="text-light text-decoration-none" href="/"
                  >Станьте парнёром-рестораном</a
                >
              </li>
            </ul>
          </div>
          <div class="col-lg-3 col-md-4 col-12 row">
            <ul class="list-link-footer">
              <li>
                <a class="text-light text-decoration-none" href="/"
                  >Все города</a
                >
              </li>
              <li class="second-smaller-element-list">
                <a class="text-light text-decoration-none" href="/">Цены</a>
              </li>
              <li class="second-smaller-element-list">
                <a class="text-light text-decoration-none" href="/">Помощь</a>
              </li>
              <li class="second-smaller-element-list">
                <a class="text-light text-decoration-none" href="/">FAQs</a>
              </li>
            </ul>
          </div>
        </section>
      </div>
      <section class="d-flex justify-content-center app-container">
        <a href="/">
          <img src="./svg/icon/App_Store.svg" alt="App Store" />
        </a>
        <a class="google-play-logo" href="/">
          <img src="./svg/icon/Google_Play.svg" alt="Google Play" />
        </a>
      </section>
      <section
        class="d-flex justify-content-between border-top user-footer-container row"
      >
        <a class="col-lg-3 col-md-3 col-3 text-user-footer" href="/"
          >© 2017 Uber Technologies Inc.</a
        >
        <a class="col-lg-3 col-md-3 col-3 text-user-footer" href="/"
          >Обработка персональных данных</a
        >
        <a
          class="col-lg-3 col-md-3 col-3 text-user-footer"
          href="/"
          >Пользовательское соглашение</a
        >
      </section>
    </div>
  </footer>
</template>

<style>
.footer-uber-eats {
  background: #262626;
}

.footer-container {
  margin-left: 80px;
  margin-right: 80px;
}

.footer-logo {
  padding-top: 55px;
}

.footer-contacts-section {
  margin-top: 40px;
}

.footer-contacts-container {
  padding-top: 32px;
  padding-bottom: 48px;
}

.language-dropdown {
  width: 100%;
}

.name-restaurant-container {
  margin-top: 33px;
  font-family: Roboto;
  font-size: 16px;
  font-weight: 400;
}

.hashtag-restaurant {
  color: #49a144;
}

@media (max-width: 767px) {
  .contacts-section {
    padding-top: 17px;
  }
}

.social-networks-container {
  margin-top: 17px;
}

.icon-social-networks {
  height: 24px;
  width: 24px;
}

.social-media-indentation {
  margin-left: 12px;
}

.label-restaurant {
  color: white;
}

.link-footer-container {
  margin-left: 100px;
}

.list-link-footer {
  list-style: none;
  cursor: pointer;
  font-family: Roboto;
  font-size: 13px;
  font-weight: 400;
}

.second-smaller-element-list {
  margin-top: 23px;
}

.app-container {
  margin-top: 40px;
  margin-bottom: 40px;
}

.google-play-logo {
  margin-left: 40px;
}

.user-footer-container {
  padding-top: 40px;
  height: 90px;
}

.text-user-footer {
  color: white;
  font-family: Roboto;
  font-size: 11px;
  font-weight: 400;
  margin: 0px;
  text-decoration: none;
  display: inline-block;
}
</style>
