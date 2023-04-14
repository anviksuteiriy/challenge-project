<template>
  <div class="footer__background">
    <div class="footer__links">
      <div class="footer__link--small">
        <div class="footer__link--info">
          <img width="199" height="80" src="https://www.lummoshop.co.id/wp-content/uploads/2021/12/lummo-shop-footer-logo-300x119.png" alt="logo">
          <p>LummoSHOP membantu kamu untuk membuat website toko online kamu dengan Mudah, Aman, dan GRATIS!</p>
          <p style="font-weight: 400;">2022 © PT BeeGroup Financial Indonesia, a subsidiary of Tulp Street Pte. Ltd. All Rights Reserved</p>
        </div>
        <div class="footer__link">
          <div class="footer__main">Produk</div>
          <p>
            <a class="available__link" href="#">
              Unduh LummoSHOP
            </a>
          </p>
          <p>
            <a class="available__link" href="#">
              LummoSHOP Plus
            </a>
          </p>
          <p>
            <a class="available__link" href="#">
              Toko Online
            </a>
          </p>
          <p>
            <a class="available__link" href="#">
              Jualan Online
            </a>
          </p>
          <p>
            <a class="available__link" href="#">
              Syarat & Ketentuan
            </a>
          </p>
          <p>
            <a class="available__link" href="#">
              Kebijakan Privasi
            </a>
          </p>
        </div>
      </div>
      <div class="footer__link--small">
        <div class="footer__link">
          <div class="footer__main">Bantuan</div>
          <a href="#" class="available__link">
            <p>FAQ</p>
          </a>
          <a href="#" class="available__link">
            <p>Pusat Edukasi</p>
          </a>
          <a href="#" class="available__link">
            <p>Testimoni Pengguna</p>
          </a>
          <a href="#" class="available__link">
            <p>Tool Bisnis</p>
          </a>
          <a href="#" class="available__link">
            <p>Kontak Kami</p>
          </a>
          <a href="#" class="available__link">
            <p>Careers</p>
          </a>
        </div>
        <div class="footer__link">
          <div class="footer__main">CONNECT</div>
          <a href="#" class="available__link">
            <p><i class="fa fa-twitter"></i> Twitter</p>
          </a>
          <a href="#" class="available__link">
            <p><i class="fa fa-facebook"></i> Facebook</p>
          </a>
          <a href="#" class="available__link">
            <p><i class="fa fa-instagram"></i> Instagram</p>
          </a>
          <a href="#" class="available__link">
            <p><i class="fa fa-youtube"></i> Youtube</p>
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>

</script>

<style scoped>
.footer__background {
  background-color: #eef2ff !important;
  height: 100%;
  width: 100%;
  padding: var(--spacing-24) 0;
}

.footer__links {
  display: flex;
  padding: var(--spacing-4) var(--spacing-12);
  justify-content: space-between;
  max-width: var(--external);
  margin: auto;
}

.available__link {
  color: #333;
  text-decoration: none;
}

.available__link p:hover {
  color: var(--project-blue);
}

.available__link:hover {
  color: var(--project-blue);
}

.footer__link--info,
.footer__link {
  color: #333;
  font-size: 15px;
  font-weight: 600;
  line-height: 1.4;
  text-align: left;
  margin-right: var(--spacing-24);
  max-width: 220px;
}

.footer__link--info {
  color: var(--project-blue);
}

.footer__main {
  color: var(--project-blue);
  font-size: 20px;
  font-weight: bold;
  line-height: 1.4;
}

.footer__notice {
  display: flex;
  color: #8e919d;
  justify-content: space-between;
  padding: 0 var(--spacing-12);
  max-width: var(--external);
  margin: auto;
}

.notice__text {
  font-size: 18px;
}

.footer__link--small {
  display: flex;
  width: 50%;
  justify-content: space-around;
}

.link__disabled {
  opacity: var(--opacity-25);
}

@media screen and (max-width: 1200px) {
  .footer__link--small {
    width: 100%;
  }
}

@media screen and (max-width: 950px) {
  .footer__links {
    flex-direction: column;
    align-items: center;
    text-align: center;
  }
  .footer__link--info,
  .footer__link {
    margin-right: 0;
    text-align: center;
  }

  .footer__link--small {
    flex-direction: column;
    width: unset;
    justify-content: unset;
  }

  .footer__notice {
    flex-direction: column;
    align-items: center;
  }

  .footer__notice p {
    text-align: center;
  }
}

@media screen and (max-width: 500px) {
  .footer__links {
    flex-wrap: wrap;
  }

  .footer__link--info,
  .footer__link {
    margin: var(--spacing-4);
    font-size: 16px;
    text-align: center;
  }
}
</style>
