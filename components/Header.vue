<template>
    <div>
      <div class="header">
        <div class="header__top">
            <div class="header__toparea">

            </div>

            <div class="header__toparea">

            </div>

            <div class="header__toparea">

            </div>
        </div>

        <div class="header__bottom">
            <div class="header__bottomarea">
                <span class="link">
                    <NuxtLink to="/link">
                        about
                    </NuxtLink>
                </span>
                <span class="link">
                    <NuxtLink to="/link">
                        journal
                    </NuxtLink>
                </span>  
            </div>
            <div class="header__bottomarea">
                <span class="logo">GIGI & OLIVE</span>
            </div>
            <div class="header__bottomarea">
                <span class="link">
                    <NuxtLink to="/link">
                        shop
                    </NuxtLink>
                </span>
                <span class="link">
                    <NuxtLink to="/link">
                        Link
                    </NuxtLink>
                </span>
                <span class="link">
                    <NuxtLink to="/link">
                        Link
                    </NuxtLink>
                </span>
            </div>
        </div>


        <div class="header__photos">
            <figure>
                <img src="https://images.unsplash.com/photo-1560106556-a8edcf61e758?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2342&q=80"/>
                <div class="header__promotion">
                    <p>We Picked Every item With Care</p>
                    <p>You Just Have To Try Them</p>
                    <p class="sub">Use this code to receive 50%</p>

                    <span class="gobtn">
                        <NuxtLink to="/promotion">
                            <span>Go To Collection</span>
                        </NuxtLink>
                    </span>
                </div>
            </figure>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
  
  }
  </script>
  
  <style lang="scss" scoped>
  .header {

    &__bottom {
        display: flex;
        align-items: center;
        justify-content: center;
    }

    &__toparea {
        background: $primary-color;
        height: #{scaleValue(20)};
    }

    &__bottomarea {
        margin: 0 #{scaleValue(20)};
        padding: #{scaleValue(20)} #{scaleValue(100)};

        & span {
            display: inline-block;

            &.logo {
                font-family: 'Baskervville', serif;
                font-size: #{scaleValue(35)};
                letter-spacing: #{scaleValue(3)};
                color: $black;
            }

            &.link {
                margin: 0 #{scaleValue(20)};
                transform: translateY(#{scaleValue(-1)});

                & a {
                    text-decoration: none;
                    color: $font-color;
                    text-transform: uppercase;
                    font-size: #{scaleValue(14)};
                    font-weight: 500;
                    letter-spacing: #{scaleValue(3)};
                }
            }
        }
    }

    &__photos {

        & figure {
            height: #{scaleValue(700)};
            position: relative;

            &::before {
                content: '';
                position: absolute;
                top: 0;
                left: 0;
                height: 100%;
                width: 100%;
                background: rgba(0,0,0,.3);
                z-index: 2;
            }

            & img {
                position: absolute;
                top: 0;
                left: 0;
                object-fit: cover;
                height: 100%;
                width: 100%;
                z-index: 1;
            }
        }
    }

    &__promotion {
        background: $white;
        position: absolute;
        bottom: #{scaleValue(150)};
        left: #{scaleValue(100)};
        z-index: 3;
        border-radius: 3px;
        padding: #{scaleValue(20)};

        & p {
            font-size: #{scaleValue(35)};
            font-weight: 400;
            line-height: #{scaleValue(45)};
            margin-top: #{scaleValue(10)};

            &.sub {
                font-size: #{scaleValue(15)};
            }
        }

        & span {
            display: inline-block;
            &.gobtn {
                margin-top: #{scaleValue(40)};
                background: $black;
                padding: #{scaleValue(15)} #{scaleValue(20)};
                border-radius: 3px;


                & a {
                    text-decoration: none;
                    color: $white;
                    font-size: #{scaleValue(15)};
                }
            }
        } 
    }
  }
  </style>
  