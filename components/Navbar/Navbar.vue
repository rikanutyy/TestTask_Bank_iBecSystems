<template>
<div class="Navbar">
 <div class="container">

  <div class="row">
    <div class="user_block col-md-12 col-lg-1">
      <div class="profile d-flex">
        <div class="profile__avatar"></div>
        <div class="profile__name">
          <h2>My Account</h2>
        </div>
      </div>
    </div><!-- col-lg(1) END -->
    <div class="nav_block col-lg-11 ml-auto">
      <nav>
        <ul class="menu d-flex">
          <li class="menu__item">
            <!-- роут ссылки 'Главная' -->
            <nuxt-link exact active-class="active" class="menu__link" to="/">
              <span>Главная</span>
            </nuxt-link>
          </li>
          
          <li class="menu__item"><a class="menu__link" href="#">Счета</a></li>
          <li class="menu__item"><a class="menu__link" href="#">Платежи</a></li>

          <li class="menu__item">
            <a class="menu__link" href="#" data-toggle="dropdown" role="button">Переводы</a>
              <!-- Выпадающее меню -->
              <div class="dropdown-menu">
                <a class="dropdown__item" href="#">На свой счет внутри банка</a>
                <a class="dropdown__item" href="#">На чужой счет внутри банка</a>
                <a class="dropdown__item" href="#">В другой банк в национальной валюте</a>
                <a class="dropdown__item" href="#">Международные платежи SWIFT</a>
              </div><!-- dropdown-menu END -->
            </li>
          <li class="menu__item"><a class="menu__link" href="#">Купля/продажа валюты</a></li>
          <li class="menu__item"><a class="menu__link" href="#">Заявки</a></li>

          <li class="menu__item">
            <!-- роут ссылки 'О нас' -->
            <nuxt-link active-class="active" class="menu__link" to="/users">
              <span>О нас</span>
            </nuxt-link>
          </li>

          <li class="menu__item">
            <!-- роут ссылки 'Контакты' -->
            <nuxt-link active-class="active" class="menu__link" to="/contacts">
              <span>Наши контакты</span>
            </nuxt-link>
          </li>

        </ul>
      </nav>
    </div><!-- col-lg(2) END -->
  </div><!-- row END -->

 </div><!-- container END -->
</div><!-- Navbar END -->
</template>

<style lang="scss">
.Navbar {
  margin-top: $default-indent;
}
.profile {
  position: relative;
  .profile__name {
      position: absolute;
      min-width: 150px;
      h2 {
        color: $heading-text-color;
        font-size: $profile-font-size;
        position: relative;
        left: 150px;
      }
  }
  .profile__avatar {
    min-width: 97px;
    height: 97px;
    background-color: $avatar-color;
    position: relative;
  }
}
.menu {
  background: $navbar-color;
  outline: none;
  border-radius: 5px;
  border: $navbar-border;
  align-items: stretch;

  margin-left: 50px;
  .menu__item {
    padding: 9px 18px;
    white-space: nowrap;
    /* border-границы */
    &:nth-child(1n) {border-right: $navbar-border}
    &:last-child {border-right: 0;}
  }
  .menu__item:hover a{
    color: $hover-color;
    transition: all 0.3s;
  }
  .active span {
    color: $active-color;
  }
  .menu__link {
    color: $text-color;
    font-size: $link-font-size;
  }
}
.dropdown-menu {
  background: $dropdown-menu-color;
  transform: translate3d(279px, 40px, 0px) !important;

  a:hover {
    color: $hover-color;
    background: $hover-background;
    transition: all 0.3s;
  }
  .dropdown__item {
    display: block;
    font-size: $dropdown-link-fs;
    width: 100%;
    padding: .25rem 1.5rem;
    clear: both;
    font-weight: 400;
    color: $text-color;
    text-align: inherit;
    white-space: nowrap;
    background-color: transparent;
    border: 0;
  }
}
.user_block {
  align-self: flex-end!important;
}
.nav_block {
  align-self: flex-end!important;
}
</style>
