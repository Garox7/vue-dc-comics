<template>
  <footer>
    <div class="footer__top">
      <div class="footer__top__container">
        <div class="footer__link">
          <div class="link">
            <ul>
              <h3>dc comics</h3>
              <li><a href="#!">Characters</a></li>
              <li><a href="#!">Comics</a></li>
              <li><a href="#!">Movies</a></li>
              <li><a href="#!">Tv</a></li>
              <li><a href="#!">Games</a></li>
              <li><a href="#!">Videos</a></li>
              <li><a href="#!">News</a></li>
            </ul>
            <ul>
              <h3>shop</h3>
              <li><a href="#!">Shop DC</a></li>
              <li><a href="#!">Shop DC Collectables</a></li>
            </ul>
          </div>
          <div class="link">
            <ul>
              <h3>dc</h3>
              <li><a href="#!">Term Of Use</a></li>
              <li><a href="#!">Privaxy Polici (New)</a></li>
              <li><a href="#!">Ad Choise</a></li>
              <li><a href="#!">Advertising</a></li>
              <li><a href="#!">Jobs</a></li>
              <li><a href="#!">Subscription</a></li>
              <li><a href="#!">Talent workshop</a></li>
              <li><a href="#!">CPSC Certificates</a></li>
              <li><a href="#!">Ratings</a></li>
              <li><a href="#!">Shop Help</a></li>
              <li><a href="#!">Contact Us</a></li>
            </ul>
          </div>
          <div class="link">
            <ul>
              <h3>sites</h3>
              <li><a href="#!">DC</a></li>
              <li><a href="#!">MAD magazine</a></li>
              <li><a href="#!">DC Kids</a></li>
              <li><a href="#!">DC Universe</a></li>
              <li><a href="#!">DC Power Visaå</a></li>
            </ul>
          </div>
        </div>
        <div class="footer__logo">
          <img src="@/img/dc-logo-bg.png" alt="">
        </div>
      </div>
    </div>
    <div class="footer__bottom">
      <div class="footer__bottom__container">
        <button>sign-up now!</button>
        <div class="footer__social">
          <h2>follow us</h2>
          <img src="@/img/footer-facebook.png" alt="Facebook">
          <img src="@/img/footer-twitter.png" alt="Twitter">
          <img src="@/img/footer-youtube.png" alt="You Tube">
          <img src="@/img/footer-pinterest.png" alt="Pinterest">
          <img src="@/img/footer-periscope.png" alt="Periscope">
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'FooterPage',
};
</script>

<style lang="scss" scoped>
$footer-width-size: 900px;

.footer__top {
  background-image: url(@/img/footer-bg.jpg);
  background-position: center;
  background-size: cover;
  width: 100%;
  height: 350px;
  display: flex;
  justify-content: center;
  overflow: hidden;
}

.footer__top__container {
  flex: 1 1 auto;
  max-width: $footer-width-size;
  display: flex;
  align-items: center;
  justify-content: space-between;

  .footer__link {
    display: flex;
    gap: 1rem;

    ul {
      &:first-child {
        margin-bottom: 1.5rem;
      }

      h3 {
        color: white;
        font-size: 16px;
        text-transform: uppercase;
        margin-bottom: .7rem;
      }

      li {
        list-style: none;

        a {
          color: rgba(255, 255, 255, 0.47);
          font-size: 16px;
          transition: all .15s ease-in-out;

          &:hover {
            color: white;
            text-decoration: underline;
          }
        }
      }
    }
  }

  .footer__logo img {
    height: 450px;
    width: 450px;
  }
}

.footer__bottom {
  width: 100%;
  background-color: rgb(48, 48, 48);
  display: flex;
  justify-content: center;
}

.footer__bottom__container {
  flex: 1 1 auto;
  max-width: 900px;
  height: 80px;
  display: flex;
  justify-content: space-between;
  align-items: center;

  button {
    background-color: transparent;
    color: white;
    font-weight: bold;
    text-transform: uppercase;
    height: 40px;
    width: 130px;
    border: 2px solid rgb(56, 128, 241);
    cursor: pointer;
    transition: all .15s linear;

    &:hover {
      background-color: rgb(56, 128, 241);
    }
  }

  .footer__social {
    display: flex;
    align-items: center;
    gap: .8rem;

    h2 {
      font-size: 20px;
      text-transform: uppercase;
      color: rgb(56, 128, 241);
    }

    img {
      border-radius: 50%;
      width: 35px;
      transition: all .2s linear;

      &:hover {
        scale: 1.1;
        cursor: pointer;
      }
    }

  }
}
</style>
