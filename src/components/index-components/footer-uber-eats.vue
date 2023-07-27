<template>
  <footer class="footer-uber-eats">
    <div class="footer-container">
      <div class="footer-logo">
        <img src="./svg/uber-eats-logo2.svg" alt="uber eats" />
      </div>
      <div class="footer-contacts-section border-top border-bottom">
        <div class="d-flex footer-contacts-container">
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
          <div class="link-footer-container col-lg-3 col-md-4 col-12">
            <ul class="list-link-footer">
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
          <div class="link-footer-container col-lg-3 col-md-4 col-12">
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
        </div>
      </div>
      <div class="d-flex justify-content-center app-container">
        <a href="/">
          <img src="./svg/icon/App_Store.svg" alt="App Store" />
        </a>
        <a class="google-play-logo" href="/">
          <img src="./svg/icon/Google_Play.svg" alt="Google Play" />
        </a>
      </div>
      <div
        class="d-flex justify-content-between border-top user-footer-container"
      >
        <span class="col-lg-3 col-md-3 col-12 text-user-footer">
          © 2017 Uber Technologies Inc.
        </span>
        <span class="col-lg-3 col-md-3 col-12 text-user-footer">
          Обработка персональных данных
        </span>
        <span class="col-lg-3 col-md-3 col-12 text-user-footer">
          Пользовательское соглашение
        </span>

        <a href="#" class="button-to-up">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="80"
            height="80"
            viewBox="0 0 80 80"
            fill="none"
          >
            <path
              fill-rule="evenodd"
              clip-rule="evenodd"
              d="M0 2C0 0.895429 0.895431 0 2 0H78C79.1046 0 80 0.895431 80 2V78C80 79.1046 79.1046 80 78 80H2C0.895429 80 0 79.1046 0 78V2Z"
              fill="#59BD5A"
            />
            <path
              d="M40.0183 27.0428L40.0527 27.0103L47.6741 34.2576L46.0754 35.7071L40.9286 30.8839V52H39.1428V30.8522L33.962 35.7071L32.3995 34.2576L40.0031 27.0103L40.0187 27.0428H40.0183Z"
              fill="white"
            />
          </svg>
        </a>
      </div>
    </div>
  </footer>
</template>

<style>
.footer-uber-eats {
  background: #262626;
}

.footer-container {
  margin-left: 60px;
  margin-right: 60px;
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
}

.button-to-up {
  position: relative;
  bottom: 50px;
  left: 40px;
}
</style>
