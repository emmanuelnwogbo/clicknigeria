<template>
    <div>
      <div class="footer">
        <div class="footer__body">
            <p class="footer__header">
                Sign up to receive updates on our latest news and offers
            </p>

            <form class="footer__form">
                <div class="footer__formarea">
                    <input class="footer__formarea--input" placeholder="enter name" ref="name"/>
                    <label class="footer__formarea--label">enter name</label>
                </div>
                <div class="footer__formarea">
                    <input class="footer__formarea--input" placeholder="enter email" type="email" ref="email"/>
                    <label class="footer__formarea--label">enter email</label>
                </div>
                <div class="footer__formarea buttonarea">
                    <span class="footer__formarea--btn">
                        submit
                    </span>
                </div>
            </form>

            <div class="footer__bottom">
                <p class="footer__header">
                    contact us
                </p>

                <div class="footer__links">
                    <div class="footer__linksarea">
                        <div class="footer__link">
                            <NuxtLink to="/shipping">
                                shipping
                            </NuxtLink>
                        </div>

                        <div class="footer__link">
                            <span class="text">+234 01207 75799</span>
                        </div>

                        <div class="footer__link">
                            <NuxtLink to="/terms">
                                terms and conditions
                            </NuxtLink>
                        </div>
                    </div>

                    <div class="footer__linksarea">
                        <div class="footer__link">
                            <NuxtLink to="/shipping">
                                returns and exchanges
                            </NuxtLink>
                        </div>

                        <div class="footer__link">
                            <span class="text">hello@mail.com</span>
                        </div>

                        <div class="footer__link">
                            <NuxtLink to="/terms">
                                privacy policy
                            </NuxtLink>
                        </div>
                    </div>

                    <div class="footer__linksarea">
                        <div class="footer__link">
                            <NuxtLink to="/shipping">
                                returns and exchanges
                            </NuxtLink>
                        </div>

                        <div class="footer__link">
                            <span class="text">hello@mail.com</span>
                        </div>

                        <div class="footer__link">
                            <NuxtLink to="/terms">
                                privacy policy
                            </NuxtLink>
                        </div>
                    </div>
                </div>

            </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    
  }
  </script>
  
  <style lang="scss" scoped>
  .footer {
    background: $primary-color-giftarea;
    margin-top: #{scaleValue(130)};

    &__body {
        @include section;
        padding-top: #{scaleValue(20)};
    }

    &__bottom {
        display: flex;
        align-items: center;
        flex-direction: column;
    }

    &__header {
        @include cardlabel;
        font-size: #{scaleValue(13)};
    }

    &__links {
        display: flex;
        justify-content: space-between;
        width: 100%;
        transform: translateY(#{scaleValue(-15)});
    }

    &__linksarea {
        display: flex;
        justify-content: space-between; 
        flex-direction: column;
    }

    &__link {
        display: flex;
        justify-content: center;

        & a {
            text-decoration: none;
            @include cardlabel;
            color: $font-color;
            font-size: #{scaleValue(12)};
        }

        & span {

            &.text {
                text-decoration: none;
                @include cardlabel;
                color: $font-color;
                font-size: #{scaleValue(13)};
            }
        }
    }

    &__form {
        display: flex;
        justify-content: center;
    }

    &__formarea {
        display: flex;
        position: relative;
        border-bottom: 2px solid rgba($black, .4);
        width: #{scaleValue(550)};
        margin-top: #{scaleValue(50)};
        margin-bottom: #{scaleValue(50)};

        &.buttonarea {
            justify-content: flex-end;
            width: #{scaleValue(150)};

            & span {
                display: inline-block;

                &.footer__formarea--btn {
                    outline: none;
                    border: none;
                    font-size: #{scaleValue(13)};
                    letter-spacing: #{scaleValue(4)};
                    background: none;
                    text-transform: uppercase;
                    font-weight: 300;
                    transform: translateY(#{scaleValue(3)});
                    cursor: pointer;

                    transition: all .3s ease-in;

                    &:hover {
                        transform: translateY(#{scaleValue(-3)});
                    }
                }
            }
        }

        &--input {
            position: relative;
            border: none;
            outline: none;
            background: transparent;
            width: 100%;
            z-index: 2;
            font-size: #{scaleValue(17)};
            padding-bottom: #{scaleValue(2)};

            &::placeholder {
                opacity: 0;
                font-size: #{scaleValue(15)};
            }

            &:placeholder-shown {

                & ~ label {
                    @include cardlabel;
                    color: $font-color;
                    transform: translateY(#{scaleValue(-7)});
                    margin: 0;
                    padding: 0;
                    font-weight: 300;
                    z-index: 1;
                    font-size: #{scaleValue(13)};
                }
            }

            &:focus {

                & ~ label {
                    font-size: #{scaleValue(9)};
                    transform: translateY(#{scaleValue(-28)});
                }
            }
        }

        &--label {
            @include cardlabel;
            color: $font-color;
            transform: translateY(#{scaleValue(-7)});
            margin: 0;
            padding: 0;
            font-weight: 300;
            z-index: 1;
            position: absolute;
            display: inline-block;
            transition: all .3s ease-in;
            font-size: #{scaleValue(9)};
            transform: translateY(#{scaleValue(-28)});
        }
    }
  }
  </style>