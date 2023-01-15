<template>
    <div>
      <section class="sectionareavi">
        <div class="sectionareavi__copyarea">
            <h2 class="sectionareavi__h2">
                <span>the</span>
                <span>gifting emporium</span>
            </h2>

            <p class="sectionareavi__copy">Sed porttitor lectus nibh. Vivamus magna justo, lacinia eget consectetur sed, convallis at tellus. Sed porttitor lectus nibh. Quisque velit nisi, pretium ut lacinia in, elementum id enim</p>
        </div>

        <div class="sectionareavi__cards">
            <div class="sectionareavi__card">
                <figure>
                    <img src="https://images.unsplash.com/photo-1592833578500-1082e18665a3?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1480&q=80"/>
                </figure>
                <p>Shop Sleepover</p>
                <span class="sectionareavi__card--line"></span>
            </div>

            <div class="sectionareavi__card">
                <figure>
                    <img src="https://images.unsplash.com/photo-1591348278863-a8fb3887e2aa?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1417&q=80"/>
                </figure>
                <p>Shop for friends</p>
                <span class="sectionareavi__card--line"></span>
            </div>

            <div class="sectionareavi__card">
                <figure>
                    <img src="https://images.unsplash.com/photo-1573162201267-83bddd2a5f0d?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=987&q=80"/>
                </figure>
                <p>Shop accessories</p>
                <span class="sectionareavi__card--line"></span>
            </div>
        </div>
      </section>
    </div>
  </template>
  
  <script>
  export default {
    
  }
  </script>
  
  <style lang="scss" scoped>
  .sectionareavi {
    @include section;

    &__copyarea {
        @include copyarea;
    }

    &__h2 {
        @include h2;
    }

    &__copy {
        font-family: 'Homemade Apple', cursiv;
        font-size: #{scaleValue(15)};
        width: 80%;
        color: $font-color;
    }

    &__cards {
        display: flex;
        justify-content: space-between;
    }

    &__card {
        width: #{scaleValue(450)};
        position: relative;
        display: flex;
        flex-direction: column;
        align-items: center;

        padding-bottom: #{scaleValue(35)};

        &--line {
            @include sectionline;
        }
        
        &:nth-child(2) {
            margin: 0 #{scaleValue(25)};
        }

        & figure {
            width: 100%;
            height: #{scaleValue(400)};

            & img {
                @include baseimg;
            }
        }

        & p {
            @include cardlabel
        }
    }
  }
  </style>