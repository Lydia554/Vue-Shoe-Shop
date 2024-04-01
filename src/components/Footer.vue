<template>
  <footer class="footer">
    <div class="footer__content">
      <div class="footer__content__deco-bar"></div>
      <div class="footer__content__first-line">
        <img
          src="../assets/shared/desktop/logo.svg"
          alt="Shoe-Shop logo"
          class="footer__content__first-line__logo"
        />
        <ul class="footer__content__first-line__link-list">
          <li class="footer__content__first-line__link-list__link">
            <router-link @click="scrollToTop" to="/">Home</router-link>
          </li>
          <li class="footer__content__first-line__link-list__link">
            <router-link @click="scrollToTop" to="/category/shoes"
              >shoes</router-link
            >
          </li>
          <li class="footer__content__first-line__link-list__link">
            <router-link @click="scrollToTop" to="/category/women"
              >women</router-link
            >
          </li>
          <li class="footer__content__first-line__link-list__link">
            <router-link @click="scrollToTop" to="/category/men"
              >men</router-link></li>

            <li class="footer__content__first-line__link-list__link">
            <router-link @click="scrollToTop" to="/components/"
              >contact</router-link>
          </li>
        </ul>
      </div>
      <p class="footer__content__text">
        Shoe-Shop is here to fulfill your footwear needs. We're a
        small team of shoe lovers and sound specialists who are devoted to
        helping you get the most out of personal collections. </p>

        <div class="footer__contact">
        <h4>Contact</h4>
            <p>Address: 562 Wellington Road, Street 32, San Francisco</p>
            <p>Phone: +01 2222 365 /(+91) 01 2345 6789</p>
            <p>Hours: 10:00 - 18:00, Mon - Sat</p>
          </div>
          <iframe
              style="border: 0; width: 100%; height: 350px"
              src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d12097.433213460943!2d-74.0062269!3d40.7101282!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0xb89d1fe6bc499443!2sDowntown+Conference+Center!5e0!3m2!1smk!2sbg!4v1539943755621"
              frameborder="0"
              allowfullscreen
            ></iframe>
        <div class="footer__content__text2" >
            <h4>About</h4>
            <a href="#">About Us</a>
            <a href="#">Delivery Information</a>
            <a href="#">Privacy Policy</a>
            <a href="#">Terms & Conditions</a>
            <a href="#">Contact Us</a>
        </div>
        <div class="footer__content__text2">
            <h4>My Account</h4>
            <a href="#">Sign In</a>
            <a href="#">View Cart</a>
            <a href="#">My Wishlist</a>
            <a href="#">Track My Order</a>
            <a href="#">Help</a>
        </div>

        
        <div class="footer-newsletter">
              <h4>Join Our Newsletter</h4>
              <p>
                Would you like exciting insights and valuable tips about our products? 
              </p>
              <p>Then sign up for our newsletter!</p>
              <form action="" method="post">
                <input type="email" name="email" /><input
                  type="submit"
                  value="Subscribe"
                />
              </form>

            </div>
      <div class="footer__content__copyright-section">
        <p class="footer__content__copyright-section__copyright-text">
          Copyright 2023. All Rights Reserved
        </p>
        <ul class="footer__content__copyright-section__social-media-links">
          <li
            class="footer__content__copyright-section__social-media-links__link">
            <router-link to="#" aria-label="Go to our Facebook"
              ><i class="fab fa-facebook fa-2x"></i
            ></router-link>
          </li>
          <li
            class="footer__content__copyright-section__social-media-links__link">
            <router-link to="#" aria-label="Go to our Twitter"
              ><i class="fab fa-twitter fa-2x"></i
            ></router-link>
          </li>
          <li
            class="footer__content__copyright-section__social-media-links__link">
            <router-link to="#" aria-label="Go to our Instagram"
              ><i class="fab fa-instagram fa-2x"></i
            ></router-link>
          </li>
        </ul>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer",
  methods: {
    scrollToTop() {
      window.scrollTo(0, 0);
    },
  },
};
</script>

<style lang="scss" scoped>
.footer {
  background: black;
  display: flex;
  flex-direction: column;
  align-items: center;

  @media (min-width: 768px) {
    align-items: flex-start;
    padding: 0 4rem 4.6rem 4rem;
  }

  * {
    color: white;
    text-align: center;
  }

  &__content {
    display: flex;
    align-items: center;
    flex-direction: column;
    

    @media (min-width: 768px) {
      margin: 0 auto;
      width: 68.9rem;
      align-items: flex-start;
    }

    @media (min-width: 1205px) {
      width: 111rem;
    }

    &__deco-bar {
      width: 10.1rem;
      height: 0.4rem;
      border-top: 0.4rem solid #b80000;
    }

    &__first-line {
      display: flex;
      flex-direction: column;
      align-items: center;
      width: 100%;

      @media (min-width: 768px) {
        align-items: flex-start;
      }

      @media (min-width: 1205px) {
        flex-direction: row;
        align-items: center;
        justify-content: space-between;
        margin-top: 7.1rem;
      }

      &__logo {
        margin: 4.8rem 0;

        @media (min-width: 768px) {
          margin: 5.6rem 0 3.2rem 0;
        }

        @media (min-width: 1205px) {
          margin: 0;
        }
      }

      &__link-list {
        @media (min-width: 768px) {
          display: flex;
          align-items: center;
        }

        &__link {
          margin-bottom: 1.6rem;
          font-weight: 700;
          font-size: 1.3rem;
          line-height: 2.5rem;
          letter-spacing: 0.2rem;
          text-transform: uppercase;

          * {
            transition: all 0.3s ease;
          }

          @media (min-width: 768px) {
            margin: 0;
            margin-right: 3.4rem;
          }

          &:hover * {
            color: #b80000;
          }

          &:last-child {
            margin-bottom: 0;
            margin-right: 0;
          }
        }
      }
    }

    &__text {
      margin: 4.8rem auto;
      color: #808080;
      font-weight: 500;
      font-size: 1.7rem;
      line-height: 2.5rem;
      width: 32.7rem;

   

      @media (min-width: 768px) {
        text-align: left;
        margin: 3.2rem 0 8rem 0;
        width: 68.9rem;
      }

      @media (min-width: 1205px) {
        width: 54rem;
      }
    }

    &__copyright-section {
      display: flex;
      flex-direction: column;
      align-items: center;

      @media (min-width: 768px) {
        flex-direction: row;
        justify-content: space-between;
        width: 100%;
      }

      &__copyright-text {
        color: #878787;
        font-weight: 700;
        font-size: 1.5rem;
        line-height: 2.5rem;
      }

      &__social-media-links {
        display: flex;
        align-items: center;
        margin: 4.8rem 0 3.8rem 0;

        @media (min-width: 768px) {
          margin: 0;
        }

        &__link {
          margin-right: 1.6rem;

          & i {
            transition: all 0.3s ease;
          }

          &:hover i {
            color: #ff0404;
          }

          &:last-child {
            margin-right: 0;
          }
        }
      }
    }
  }
}
.footer__content__text2 {
        display: flex;
    flex-direction: column;
    align-items: flex-start;
    margin-bottom: 20px;
    font-size: 1.3rem;
    margin-top: 25px;
   
      }
      .footer__contact {
        display: flex;
    flex-direction: column;
    align-items: flex-start;
    margin-bottom: 50px;
    font-size: 1.5rem;
      }

      .footer__content__copyright-section {
        margin-top: 40px;
       
      }

     .footer-newsletter {
  font-size: 15px;
}
.footer-newsletter h4 {
  font-size: 25px;
  font-weight: bold;
  color: #ffffff;
  position: relative;
  padding-bottom: 12px;
}
.footer-newsletter form {
  margin-top: 30px;
  background: #fff;
  padding: 6px 10px;
  position: relative;
  border-radius: 50px;
  text-align: left;
  border: 1px solid #6b0000;
}

.footer-newsletter form input[type="email"] {
  border: 0;
  padding: 4px 8px;
  width: calc(100% - 100px);
}
.footer-newsletter p {
  font-size: 20px ;
}

.footer-newsletter form input[type="submit"] {
  position: absolute;
  top: -1px;
  right: -1px;
  bottom: -1px;
  border: 0;
  background: none;
  font-size: 16px;
  padding: 0 20px 2px 20px;
  background: #4e4343;
  color: #fff;
  transition: 0.3s;
  border-radius: 50px;
  box-shadow: 0px 2px 15px rgba(0, 0, 0, 0.1);
}

.footer-newsletter form input[type="submit"]:hover {
  background: #920000;
}




</style>
