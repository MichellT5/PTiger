# Template 002
Output Mobile

![Template 002 Mobile](t002-mobile.png)

Output Desktop

![Template 002 Desktop](t002-desktop.png)

### Code HTML

```html
<div class="secodary-ctas">
    <div class="cta-container">
        <a href="#" title="" class="cta cta-1">
            <span class="title">We have towing available!</span>
            <span class="text">We offer courtesy shuttle service for those all-day repairs.</span>
            <span class="button">Contact Us</span>
        </a>
    </div>
    <div class="cta-container">
        <a href="#" title="" class="cta cta-2">
            <span class="title">At Home In The News</span>
            <span class="text">Keep up to date with our articles and recent news</span>
            <span class="button">Read More</span>
        </a>
    </div>
</div>
```

### Code SCSS

```scss
//$prop = the property to adjust
@function get-vw-mb($prop) { $vw-result: $prop / 12.42; @return #{$vw-result}vw; }
@function get-vw-desktop($prop) { $vw-result: $prop / 19.2; @return #{$vw-result}vw; }
.secodary-ctas {
    display: flex; flex-direction: column; justify-content: center; align-items: center;
    .cta-container {
        .cta {
            display: flex; flex-direction: column; justify-content: center; align-items: center; height: get-vw-mb(528);
            width: get-vw-mb(740); margin: get-vw-mb(25) 0; font-family: $webfont; text-align: center; background-color: $primary-color;
            color: $third-color; text-decoration: none;
            .title {
                font-weight: 700; font-size: get-vw-mb(74); }
            .text {
                font-size: get-vw-mb(46); padding-top: get-vw-mb(20); }
            .button {
                margin-top: get-vw-mb(40); border-radius: 7px; width: get-vw-mb(458); height: get-vw-mb(111); font-size: get-vw-mb(39);
                color: third; background: $secondary-color; display: flex; justify-content: center; align-items: center;
            }
        }
    }
    @media (min-width: 768px) {
        display: flex; flex-direction: row; justify-content: space-between; margin: get-vw-desktop(50);
        .cta-container {
            width: 49%;
            .cta {
                height: get-vw-desktop(528); width: 100%; margin: 0; transition: all 0.5s ease-in-out;
                .title {
                    display: flex; justify-content: center; align-items: flex-end; font-size: get-vw-desktop(66);
                    height: get-vw-desktop(149);
                }
                .text {
                    display: flex; justify-content: center; align-items: center; font-size: responsive-px(14, 28, 768, 1920);
                    padding-top: 0; height: get-vw-desktop(117); width: get-vw-desktop(416);
                }
                .button {
                    margin-top: 0; border-radius: 7px; width: get-vw-desktop(236); height: get-vw-desktop(65);
                    font-size: responsive-px(12, 21, 768, 1920);
                }
                &:hover { transform: scale(0.9); opacity: 0.9; }
            }
        }
    }
}
```