<template>
    <div>
      <div class="giftarea">
        <figure>
            <img src="https://images.unsplash.com/photo-1530530612927-9bff970e898a?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2340&q=80"/>
        </figure>

        <div class="giftarea__text">
            <h2 class="giftarea__h2">
                <span>all wrapped up</span>
            </h2>

            <p class="giftarea__copy">Sed porttitor lectus nibh. Vivamus magna justo, lacinia eget consectetur sed, convallis at tellus. Sed porttitor lectus nibh. Quisque velit nisi.</p>

            <NuxtLink to="/giftarea">
                shop gifts
            </NuxtLink>
            <span class="giftarea__copy--line"></span>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    
  }
  </script>
  
  <style lang="scss" scoped>
  .giftarea {
    @include section;
    background: $primary-color-giftarea;
    padding-top: #{scaleValue(35)};
    display: flex;
    align-items: center;
    margin: #{scaleValue(60)} 0;

    &__h2 {
        @include h2;
    }

    &__copy {
        font-family: 'Homemade Apple', cursiv;
        font-size: #{scaleValue(15)};
        width: 80%;
        color: $font-color;
        margin-bottom: #{scaleValue(30)};

        &--line {
            @include sectionline;
            width: #{scaleValue(200)};
        }
    }

    & figure {
        position: relative;
        width: 60%;
        height: #{scaleValue(550)};
        flex-shrink: 0;
        z-index: 1;

        & img {
            @include baseimg;
        }
    }

    &__text {
        position: relative;
        background: $white;
        width: 57%;
        flex-shrink: 0;
        height: #{scaleValue(470)};
        z-index: 2;
        transform: translateX(#{scaleValue(-130)});

        text-align: center;

        display: flex;
        align-items: center;
        flex-direction: column;
        padding-top: #{scaleValue(90)};

        & a {
            text-decoration: none;
            @include cardlabel;
            color: $font-color;
        }
    }
  }
  </style>