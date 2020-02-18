# Footer
The next code helps to prettier the footer.

The first two lines define the background color and a font-color to make them look like the xd file.
```scss
// ===[FOOTER]=== //
#bgbottom {
    background: #000;
    $text-color: #fff;
    font-family: $webfont; border-top: 0vw solid $primary-color;
    @include tablet-desktop { border-width: 0vw; }
    #dnn_dnnLogoFooter_hypLogo {
        position: relative; z-index: 1; display: block; margin: 9vw auto; width: 20vw; min-width: 200px; padding: 0;
        @include tablet-desktop { margin: 0 0 1vw; width: 8.52vw; min-width: 150px; padding: 0; }
        #dnn_dnnLogoFooter_imgLogo { display: block; width: 100%; }
    }
    #netdriven {
        width: 90%; max-width: 1500px; margin: 0 auto; padding: 2vw 1vw 1vw; overflow: visible;
        #BottomFooter {
            padding-top: 0; color: $text-color;
            #poweredbynd, #poweredbynd * { box-sizing: initial; text-align: left; a { color: #fff; position: absolute; } }
            #socialfont { @include max(527) { float: unset; } }
            @include tablet-desktop {
                display: flex; justify-content: flex-end;
                >* { max-width: 30%; margin: 0; padding: 0; }
            }
            h2, a:not(.dnnPrimaryAction), .captcha { color: $text-color; }
            a:not(.dnnPrimaryAction) {
                transition: color 0.3s ease-in-out;
                &:hover { text-decoration: underline; /* color: $primary-color; */ }
            }
        }
        input.mobile-c, textarea.mobile-c, #BottomFooter #EntryForm .captcha input {
            background-color: #fff; color: #000; border: 1px solid #000;
            $placeholder-color: #333 !important;
            &::-webkit-input-placeholder { color: $placeholder-color; }
            /* Firefox < 19 */ &:-moz-placeholder { color: $placeholder-color; }
            /* Firefox > 19 */ &::-moz-placeholder { color: $placeholder-color; }
            /* Internet Explorer 10 */ &:-ms-input-placeholder { color: $placeholder-color; }
        }
        #EntryForm .DynamicForms_SaveFormDiv {
            @include phone { margin: 0 auto; }
            .dnnPrimaryAction.dynamicforms_link {
                @extend %btn; @extend %btn-flex; justify-content: center; width: 100px; height: 30px;
                left: 0; outline: 0; padding: 0; text-shadow: none; box-shadow: none;
                @include phone { margin: 0 auto; }
                @include hover { background-color: $primary-color !important; }
            }
        }
        span.captcha { @include phone { text-align: center; } }
        .captcha {
            input { width: auto !important; @include phone { margin: 1vw auto; } }
            img[src*="/ImageChallenge.captcha.aspx?"] {
                float: none; position: static; display: block; margin: 0 0 5px;
                @include phone { margin: 0 auto; }
            }
        }
        #FooterPane1Container { @include tablet-desktop { width: 30%; margin-right: auto; } }
        #FooterPane2Container, #FooterPane3Container {
            font-size: 1.5em; margin: 3vw 0 0; @include tablet-desktop { padding: 0 0 0 30px; } @include max(527) { text-align: center; }
        }
        #FooterPane4Container { min-height: auto; }
    }
}
```