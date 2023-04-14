<template>
  <div>
    <nav class="navigation">
      <a
        to="/"
        style="text-decoration: none; margin-right: var(--spacing-6)"
      >
        <img class="logo__image" alt="LummoSHOP" src="https://www.lummoshop.co.id/wp-content/uploads/2021/12/lummo-shop-logo.png" />
      </a>
      <slot></slot>
      <div class="spacer"></div>

      <div class="navigation__desktop" v-click-outside="closeDropdownDesktop">
        <div>
          <a to="https://link.lummoshop.com/AXiHmasXSmb" class="nav__desktop-link">
            <span>Unduh LummoSHOP</span>
          </a>
        </div>
        <div>
          <a to="https://www.lummoshop.co.id/harga/" class="nav__desktop-link">
            <span>Upgrade LummoSHOP</span>
          </a>
        </div>
        <div @click="toggleLayanan">
          <span class="navigation__dropdowns-more nav__desktop-link">
            Layanan
            <i v-show="!layananDropdown" class="fa fa-angle-down"></i>
            <i v-show="layananDropdown" class="fa fa-angle-right"></i>
          </span>
          <div
            class="navigation__dropdown--resources--close"
            :class="visibleLayananDropdown"
          >
            <a class="partners__link">
              <span>Toko Online</span>
            </a>
            <a class="partners__link">
              <span>Pengiriman</span>
            </a>
            <a class="partners__link">
              <span>Pembayaran</span>
            </a>
          </div>
        </div>
        <div @click="toggleJelajahi">
          <span class="navigation__dropdowns-more nav__desktop-link">
            Jelajahi
            <i v-show="!jelajahiDropdown" class="fa fa-angle-down"></i>
            <i v-show="jelajahiDropdown" class="fa fa-angle-right"></i>
          </span>
          <div
            class="navigation__dropdown--aboutus--close"
            :class="visibleAboutUs"
          >
            <a to="" class="partners__link">
              <span>Blog</span>
            </a>
            <a to="/team" class="partners__link">
              <span>Event</span>
            </a>
            <a to="/team" class="partners__link">
              <span>Tool Bisnis</span>
            </a>
          </div>
        </div>
      </div>
      <div class="navigation__small" @click="toggleMobileNav">
        <div class="navigation__menu" v-show="!mobileNavVisible">
          <i class="fa fa-bars"></i>
        </div>
        <div class="navigation__menu" v-show="mobileNavVisible">
          <i class="fa fa-times"></i>
        </div>
      </div>
    </nav>
    <div class="mobile__navigation" :class="mobileNavigationVisible">
      <div class="mobile__links">
        <a to="/">
          <p class="main__links">Unduh LummoSHOP</p>
        </a>
        <a to="#">
          <p class="main__links">Upgrade LummoSHOP</p>
        </a>
        <a to="#">
          <p class="main__links">Toko Online</p>
        </a>
        <a to="#">
          <p class="main__links">Pengiriman</p>
        </a>
        <a to="#">
          <p class="main__links">Pembayaran</p>
        </a>
        <a to="#">
          <p class="main__links">Blog</p>
        </a>
        <a to="#">
          <p class="main__links">Event</p>
        </a>
        <a to="#">
          <p class="main__links">Tool Bisnis</p>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      jelajahiDropdown: false,
      mobileNavVisible: false,
      layananDropdown: false
    }
  },
  computed: {
    visibleAboutUs() {
      return {
        'navigation__dropdown--jelajahi--open':
          this.jelajahiDropdown
      }
    },
    visibleLayananDropdown() {
      return {
        'navigation__dropdown--resources--open':
          this.layananDropdown
      }
    },
    mobileNavigationVisible() {
      return {
        'mobile__navigation--open': this.mobileNavVisible
      }
    }
  },
  methods: {
    closeDropdownDesktop() {
      this.jelajahiDropdown = false
      this.layananDropdown = false
    },
    closeDropdownMobile() {
      this.mobileNavVisible = false
    },
    toggleJelajahi() {
      this.jelajahiDropdown = !this.jelajahiDropdown
      this.layananDropdown = false
    },
    toggleLayanan() {
      this.layananDropdown = !this.layananDropdown
      this.jelajahiDropdown = false
    },
    toggleMobileNav() {
      this.mobileNavVisible = !this.mobileNavVisible
    }
  }
}
</script>

<style scoped>
.navigation {
  height: 100px;
  display: flex;
  flex-direction: row;
  align-items: center;
  padding: var(--spacing-2) var(--spacing-16);
  position: relative;
  flex-wrap: wrap;
  background-color: var(--project-blue) !important;
}

.logo__image {
  width: 150px;
  height: 60px;
}
.navigation__desktop {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  min-width: 560px;
  position: relative;
  font-weight: 600;
  font-size: 14px;
  line-height: 1.4;
  margin-left: auto;
}

.partners__link,
.nav__desktop-link {
  color: #ffffff;
  text-decoration: none;
  padding: var(--spacing-2) var(--spacing-2);
}
.partners__link {
  color: #000;
}

.nav__desktop-link {
  cursor: pointer;
}

.partners__link:hover {
  cursor: pointer;
  background: #fff4e5;
}

.spacer {
  margin-left: auto;
  margin-right: auto;
}

.fa {
  margin-left: var(--spacing-2);
  font-size: 20px;
  width: 16px;
  height: 16px;
}

.navigation__dropdowns-more {
  display: flex;
  justify-content: center;
}

.partner__button {
  padding: var(--spacing-2);
  background: white;
  color: #f99110;
  box-shadow: var(--shadow-md);
  min-width: 176px;
}

.partner__button:hover {
  cursor: pointer;
}

.navigation__small {
  display: none;
}

.navigation__dropdown--aboutus--close,
.navigation__dropdown--partners--close,
.navigation__dropdown--resources--close {
  display: none;
}

.navigation__dropdown--jelajahi--open {
  display: flex !important;
  flex-direction: column;
  position: absolute;
  min-width: 150px;
  background: var(--white);
  box-shadow: var(--shadow-md);
  top: 42px;
  z-index: 1;
  right: 0;
  white-space: nowrap;
}

.navigation__dropdown--resources--open {
  display: flex !important;
  flex-direction: column;
  position: absolute;
  min-width: 150px;
  background: var(--white);
  box-shadow: var(--shadow-md);
  top: 42px;
  z-index: 1;
  white-space: nowrap;
}

.navigation__dropdown--resources--open a:hover {
  color: #f99110;
}
.navigation__dropdown--jelajahi--open a:hover {
  color: #f99110;
}

.mobile__navigation {
  display: none;
}

.link__disabled {
  opacity: var(--opacity-25);
}

@media screen and (max-width: 850px) {
  .logo__image {
    width: 100px;
    height: 40px;
  }
  .navigation__desktop {
    display: none;
  }

  .navigation__small {
    display: block;
  }

  .navigation__menu {
    display: flex;
    align-items: center;
    justify-content: space-between;
    color: white;
  }

  .navigation__menu span {
    font-size: 18px;
    font-weight: 600;
  }

  .navigation__menu:hover {
    cursor: pointer;
  }

  .mobile__navigation {
    display: none;
  }

  .mobile__navigation--open {
    display: flex;
    width: 100%;
    height: auto;
    background: var(--project-blue);
    position: absolute;
    top: 80px;
    z-index: 10;
    box-shadow: var(--shadow-md);
  }

  .mobile__links {
    padding: var(--spacing-4);
    width: 100%;
    text-align: center;
  }

  .main__links {
    color: var(--white);
    font-size: 16px;
    font-weight: 600;
    line-height: 1.4;
  }
}
</style>
