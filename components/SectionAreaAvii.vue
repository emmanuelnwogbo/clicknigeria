<template>
    <div>
      <div class="sectionareavii">
        <div class="sectionareavii__copyarea">
            <h2 class="sectionareavii__h2">
                <span>Gift it well</span>
            </h2>

            <p class="sectionareavii__copyarea--label">shop stocking fillers</p>
            <span class="sectionareavii__copyarea--line"></span>
        </div>

        <div class="sectionareavii__cards">
            <div class="sectionareavii__card">
                <figure>
                    <img src="https://images.unsplash.com/photo-1618354691373-d851c5c3a990?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1015&q=80"/>
                </figure>
                <div class="sectionareavii__carddetail">
                    <p class="sectionareavii__carddetail--productname">Silk Pyjamas</p>
                    <p class="sectionareavii__carddetail--productprice">$12.00</p>
                </div>
            </div>
            <div class="sectionareavii__card">
                <figure>
                    <img src="https://images.unsplash.com/photo-1591375275686-e9b036b15f95?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1974&q=80"/>
                </figure>
                <div class="sectionareavii__carddetail">
                    <p class="sectionareavii__carddetail--productname">Silk Pyjamas</p>
                    <p class="sectionareavii__carddetail--productprice">$12.00</p>
                </div>
            </div>
            <div class="sectionareavii__card">
                <figure>
                    <img src="https://images.unsplash.com/photo-1587303876752-91efb6315dcc?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1035&q=80"/>
                </figure>
                <div class="sectionareavii__carddetail">
                    <p class="sectionareavii__carddetail--productname">Silk Pyjamas</p>
                    <p class="sectionareavii__carddetail--productprice">$12.00</p>
                </div>
            </div>
            <div class="sectionareavii__card">
                <figure>
                    <img src="https://images.unsplash.com/photo-1492707892479-7bc8d5a4ee93?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1365&q=80"/>
                </figure>
                <div class="sectionareavii__carddetail">
                    <p class="sectionareavii__carddetail--productname">Silk Pyjamas</p>
                    <p class="sectionareavii__carddetail--productprice">$12.00</p>
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
  .sectionareavii {
    @include section;

    &__copyarea {
        @include copyarea;

        &--label {
            @include cardlabel;
            line-height: #{scaleValue(35)};
            margin-top: 0;
        }

        &--line {
            @include sectionline;
            width: #{scaleValue(280)};
        }
    }

    &__h2 {
        @include h2;
        margin-bottom: #{scaleValue(10)};
    }

    &__cards {
        display: flex;
        justify-content: space-between;
    }

    &__card {
        width: #{scaleValue(300)};

        &:nth-child(4) {
            margin: 0;
        }

        & figure {
            width: 100%;
            height: #{scaleValue(400)};
            background: $primary-color-giftarea;

            & img {
                @include baseimg;
            }
        }
    }

    &__carddetail {
        @include cardlabel
    }
  }
  </style>