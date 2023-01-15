<template>
    <div>
      <div class="plake">
       <!-- <div class="plake__area top">
            <figure>
                <img src="https://images.unsplash.com/photo-1608755727748-dfa2e44f255b?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2340&q=80"/>
            </figure>
        </div>-->

        <div class="plake__area middle">
            <figure>
                <img src="https://images.unsplash.com/photo-1566737236500-c8ac43014a67?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2340&q=80" />
            </figure>

            <div class="plake__copy">
                <p class="plake__copy--header">
                    G&O JOURNAL
                </p>
                <h2 class="plake__h2">
                    <span>Winter</span>
                    <span>wedding</span>
                    <span>inspiration</span>
                </h2>

                <p class="plake__copy--text">Sed porttitor lectus nibh. Vivamus magna justo, lacinia eget consectetur sed, convallis at tellus. Sed porttitor lectus nibh. Quisque velit nisi.</p>

                <NuxtLink to="/blog">
                    read more
                </NuxtLink>

                <span class="plake__copy--line"></span>
            </div>
        </div>

        <div class="plake__area bottom">
            <p class="plake__copy--header">
                 #Gigianandolive
            </p>

            <div class="plake__bottomcards">
                <figure class="plake__bottomcard">
                    <img src="https://images.unsplash.com/photo-1555086156-e6c7353d283f?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2340&q=80"/>
                </figure>
                <figure class="plake__bottomcard">
                    <img src="https://images.unsplash.com/photo-1504704911898-68304a7d2807?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2340&q=80"/>
                </figure>
                <figure class="plake__bottomcard">
                    <img src="https://images.unsplash.com/photo-1545128485-c400e7702796?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2340&q=80"/>
                </figure>
                <figure class="plake__bottomcard">
                    <img src="https://images.unsplash.com/photo-1533174072545-7a4b6ad7a6c3?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2340&q=80"/>
                </figure>
                <figure class="plake__bottomcard">
                    <img src="https://images.unsplash.com/photo-1504704911898-68304a7d2807?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2340&q=80"/>
                </figure>
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
  .plake {
    @include section;
    padding-top: 0;
    padding-bottom: 0;

    &__area {

        &.top {

            & figure {
                height: #{scaleValue(400)};

                & img {
                    @include baseimg;
                }
            }
        }

        &.middle {
            display: flex;
            align-items: center;

            & figure {
                height: #{scaleValue(500)};
                width: 50%;

                & img {
                    @include baseimg;
                }
            }
        }

        &.bottom {
            margin-top: #{scaleValue(130)};
        }
    }

    &__copy {
        width: 50%; 
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        padding-left: #{scaleValue(100)};

        &--header {
            @include cardlabel;
            margin-bottom: #{scaleValue(30)};
        }

        &--text {
            font-family: 'Homemade Apple', cursiv;
            font-size: #{scaleValue(15)};
            width: 80%;
            color: $font-color;
            margin-bottom: #{scaleValue(30)};
        }

        & a {
            text-decoration: none;
            @include cardlabel;
            color: $font-color;
        }

        &--line {
            @include sectionline;
            width: #{scaleValue(120)};
        }
    }

    &__h2 {
        @include h2;
    }

    &__bottomcards {
        display: flex;
        justify-content: space-between;
    }

    &__bottomcard {
        height: #{scaleValue(220)};
        width: #{scaleValue(248)};
        flex-shrink: 0;
        
        & img {
            @include baseimg;
        }
    }
  }
  </style>