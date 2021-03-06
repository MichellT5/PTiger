# PTiger
Here you would find HTML, CSS code to improve your time while building ND sites.

Look inside the folders to explore code about that section.
***
## Default
Default is a template which includes some predefined styles to facilite the build and improve times

You could replace the skin.scss content with default and start building from the end fo the file.

```scss
/*
#######################################
DEV VERSION 4.0 LAST UPDATED 2/21/2019
#######################################
*/

$primary-color: #727272;
$secondary-color: #fff;

$webfont: 'Nunito Sans', sans-serif;
$webfont2: 'Open Sans', sans-serif;

.webfont, .pc-header .Head, #BottomFooter h2{font-family:$webfont, sans-serif !important;}
.webfont2, .vlbCatalogBtn{font-family:$webfont2, sans-serif;}

.container {width:100%; max-width:980px; margin:0 auto;}

// Imports
@import 'components/media-queries';
@import 'components/master';
@import 'components/animation-effects';
@import 'components/social-icons';
@import 'components/header';
@import 'components/topbar';
@import 'components/navbar';
@import 'components/hometext';
@import 'components/footer';
@import 'components/mobile-buttons';
@import 'components/location-finder';
// @import 'components/ndsc-widget';
// @import 'components/photo-gallery';
// @import 'components/hp-review-widget';
// @import 'components/wheel-config';
@import 'components/ndsc';
@import 'components/atc';
@import 'components/location-widget';
@import 'components/instant-quote';
@import 'components/coupons';
@import 'components/ma-advisor';
@import 'components/reviews';
@import 'components/aqmodule';

/*=============================================
=            Top Bar Styles            =
=============================================*/

$topbar-color: #fff;
$topbar-fontsize: 1.4em;
$actionbar-width: 980px;

#nd-actionbar .container{max-width:$actionbar-width; padding:0;}
#dnn_ActionBarPane .quote-btn{font-size:1.2em;}
#dnn_ActionBarPane .quote-btn a{color:$topbar-color; text-decoration: none; margin-right:20px;}
#dnn_ActionBarPane .quote-btn a:last-of-type{margin:0;}
#dnn_ActionBarPane .quote-btn a:hover{text-decoration: underline;}
#dnn_ActionBarPane #top-social{display:flex; justify-content: space-between;}
#dnn_ActionBarPane #top-social a{color:$topbar-color; text-decoration: none; font-size:$topbar-fontsize; margin-right:20px; padding:1px 0;}
#dnn_ActionBarPane #top-social a:last-of-type{margin:0;}

/*============================================================================================================================*/

/*=============================================
=            Navbar Styles                   =
=============================================*/

$nav-width: 980px;
$nav-dropdown-bg: #333;
$nav-main-color: #fff;
$nav-sub-color: #fff;
$nav-hover-color: #C91919;

@include desktop{
    #contentnav{height:50px; width:$nav-width;}
}

@include tablet-desktop{
    #nd-menubar{background:#272727; z-index:15;}

    #contentnav #dnnMenu a {text-transform:uppercase; color:#FFF; display: block; font-weight:700; font-size:1em; text-decoration:none; transition:background 200ms ease-in-out; -moz-transition:background 200ms ease-in-out; -webkit-transition:background 200ms ease-in-out; }
    #contentnav #dnnMenu .topLevel li.selected > a {text-decoration: underline;} /* Current Tab */
    #contentnav #dnnMenu .subLevel li a {margin: 0px; padding: 10px 20px; line-height: normal; color:$nav-sub-color;}

    // Sub Level Menu Background Color
    #contentnav #dnnMenu .subLevel ul, #contentnav #dnnMenu .subLevel .subLevelRight ul{background-color:$nav-dropdown-bg;}

    // Default Hover Effects
    #contentnav #dnnMenu .topLevel li:hover > a{background:#373737;}
    #contentnav #dnnMenu .subLevel li a:hover{background:#474747;}

    // Sub Level Borders
    #contentnav #dnnMenu .single-column li a{border-bottom: 1px solid #888;}
    #contentnav #dnnMenu .subLevel.double-column li a{border-bottom: 1px solid #888; border-right: 1px solid #888;}
}

/*============================================================================================================================*/

/*=============================================
=            Header Styles                   =
=============================================*/

#contentheader { padding:0; height:auto; margin: 0 auto;}
#dnn_HeaderContactPane {float:right;}
#dnn_dnnLogo_imgLogo{float:left;}

#headercontact {text-transform:none; color:#fff; line-height:normal; text-align: right;}

@include desktop{
    #dnn_dnnLogo_imgLogo {margin:2% 0;}
    #dnn_HeaderContactPane {margin:2% 0 0;}
}

@include tablet{
    #dnn_dnnLogo_imgLogo{margin:100px auto 0;}
}

@include tablet-phone{
    #dnn_dnnLogo_imgLogo{padding:1% 0;}
    #headercontact{text-align: center;}
    #headercontact .phone {float:none; margin:0;}
    #headercontact .address {float:none;}
}

/*============================================================================================================================*/

/*=============================================
=            Mobile Menu Styles              =
=============================================*/
$mobile-nav-bg: 0;

@include phone{
    // Mobile Top Bar Background
    .mobileBG{background:$primary-color; opacity:$mobile-nav-bg;}

    //Mobile Menu Background
    .nd-mobile-window{background:$primary-color;}

    //Mobile Sub Level Color
    #contentnav #dnnMenu .subLevel{background:lighten($primary-color,15%) !important;}
}

/*============================================================================================================================*/

/*=============================================
=            Row Background Styles            =
=============================================*/

#nd-background { background-color: #777; background-attachment:fixed;}

.homepage #nd-middlebar::after{float:left; clear:both; content:"";}

#main-content{background:#FFF;}
#sub-content{background:#FFF;}
#bgbottom{background:#000000;}

@include phone{
    #sub-content{display: none;}
}

/*=============================================================================================================================*/

/*=============================================
=            Main Call to Action Styles      =
=============================================*/

#ctabox{display: flex; justify-content: space-around; flex-flow: row wrap; align-items: center;}
#ctabox a{flex:1 0 auto; text-align: center; text-decoration: none; background:$primary-color; color:#fff; margin:10px; box-sizing: border-box; padding:10px;}

/*===============================================================================================================================*/

/*=============================================
=            Hometext Section            =
=============================================*/

// Default Button Styles
.homepage-options{display: flex; justify-content: center; flex-wrap: wrap; flex-direction: row;}
.homepage-options a{flex:1 1 auto; @include button-bg($primary-color); min-width:15%; padding:1em; margin:.5em; text-decoration:none !important; color:#fff !important; text-transform:uppercase; text-align:center; -webkit-transition: all ease 0.8s; -moz-transition: all ease 0.8s; transition: all ease 0.8s; font-size:1em;}
.homepage-options a:hover{color:#fff !important;}

/*===============================================================================================================================*/

/*=============================================
=            NDSC Widget Styles            =
=============================================*/

#services_div {background:#fff; width:100%; height:auto; position:relative; border:0; margin:0% 0; padding:2% 0 0; overflow:hidden;}
#services_div .ndcustomcolorclass, .ndcustomcolorcontainer img, .subtitle {background-color:$primary-color !important}
#left_a, #right_a{display:block; position:absolute; top:65px; cursor:pointer; color: $primary-color; font-size: 2.5em;  text-decoration: none !important;}
#left_a{left:21px; }
#left_a:before {content:'\f104'; font-family:'Font Awesome 5 Free'; font-weight:900;}
#right_a{right:5px;}
#right_a:before {content:'\f105'; font-family:'Font Awesome 5 Free'; font-weight:900;}

/*===============================================================================================================================*/

/*=============================================
=                VLB Styles                  =
=============================================*/

// Horizontal VLB
#TireSizeFinder #sizefinder-inputs {padding:1% 0 2% 0; display:flex; justify-content: center;}
#TireSizeFinder #sizefinder-inputs select {width:100px !important; transition: all .15s ease-in-out;}
#TireSizeFinder #sizefinder-inputs div{width:130px;}
#TireSizeFinder .vlbselect{border-radius: 0 !important; border: solid transparent 1px;}	

#links {display:flex; justify-content: center; margin:0;}

.vlbCatalogBtn{background:$primary-color; font-size:1em; font-weight:700; color:#fff !important; text-align:center; text-transform:uppercase; text-decoration:none !important; transition:all 0.2s ease-in-out; -moz-transition:all 0.2s ease-in-out; -webkit-transition:all 0.2s ease-in-out; padding:.5em 3em; box-sizing:border-box; }
.vlbCatalogBtn:hover{background:#000; color:#fff !important; }
/*
#find-tire-bar .searchbuttons{margin-bottom:2%; overflow:hidden;}
#find-tire-bar .searchbuttons a{display:block; color:#05178a; width:48%; border:2px solid #05178a; font-size:12px; font-weight:700; font-family:"nimbus-sans", sans-serif; text-align:center; text-transform:uppercase; padding:5px 2px; box-sizing:border-box; transition:all 0.2s ease-in-out; -moz-transition:all 0.2s ease-in-out; -webkit-transition:all 0.2s ease-in-out; text-decoration:none;}
#find-tire-bar .searchbuttons a:hover{color:#FFF; background:#05178a; border-color:#FFF;}
*/
#find-tire-bar .searchbuttons .by-size{float:left;}
#find-tire-bar .searchbuttons .by-brand{float:right;}

@include tablet{
    #TireSizeFinder #sizefinder-inputs {margin:1% auto;}
    #links {justify-content: center; margin:0;}
    #TireSizeFinder .vlbCatalogBtn{padding:2% 10%;}
}

@include phone{
    #find-tire-bar{width:auto; height:auto; padding:2%; background-size:contain;}
    #TireSizeFinder #sizefinder-inputs{float:none; padding:2% 0; align-items: center; flex-direction: column;}
    #TireSizeFinder #sizefinder-inputs div{width: auto;}
    #TireSizeFinder #sizefinder-inputs select{width:200px !important; height:40px; padding:3% !important; margin-bottom:10px; display:block; font-size:1em !important;}
    #links{width:100%; margin:0;}
    .vlbCatalogBtn{width:100%; display:block; color:#FFF; padding:2%; color:#fff !important; background-color:$primary-color !important;}
}

/*========================================================================================================================================*/

/*=============================================
=            Coupon Section Styles            =
=============================================*/

.coupon-section #dnn_HomeSidePane{float:left; width:30%;}
.coupon-section #dnn_HomeContentPane{ float:right; width:60%;}

@include tablet{
    .check-coupons{width:100%; height:auto;}
    #dnn_HomeSidePane{width:25%; margin-left:1%;}
    #dnn_HomeContentPane{width:70%; margin-right:1%;}
}

@include phone{
    .coupon-section #dnn_HomeSidePane{display:none;}
    .coupon-section #dnn_HomeContentPane{width:100%; height:auto;}
}

/*=======================================================================================================================================*/

/*=============================================
=            Tire Brands Bar                 =
=============================================*/

#brands {text-align:center; background:#fff;}
#brands img {width:18%;}

@include phone{
    #brands{display:none;}
}

/*=======================================================================================================================================*/

/*=============================================
=               DNN Pane Styles              =
=============================================*/

#dnn_LeftPane {float:left; width:30%;}
#dnn_RightPane {float:right; width:65%;}

@include phone{
    #dnn_ContentPane, #dnn_HomeSidePane, #dnn_LeftPane, #dnn_RightPane, #dnn_HomeContentPane, #contentnav{width:auto; float:none;}
}

/*=======================================================================================================================================*/

// Custom code
@function responsive-px($sm-px, $lg-px, $sm-vw, $lg-vw) { @return calc(#{$sm-px}px + (#{$lg-px} - #{$sm-px}) * ((100vw - #{$sm-vw}px) / (#{$lg-vw} - #{$sm-vw}))); }
@function responsive-px-extra($sm-px, $lg-px, $sm-vw, $lg-vw, $extra: 0px) { @return calc(#{$sm-px}px + (#{$lg-px} - #{$sm-px}) * ((100vw - #{$sm-vw}px) / (#{$lg-vw} - #{$sm-vw})) + #{$extra}); }
@function get-vw-mb($px) { $vw-result: $px / 12.42; @return #{$vw-result}vw; }
@function get-vw-desktop($px) { $vw-result: $px / 19.2; @return #{$vw-result}vw; }
@mixin hoverall { &:hover, &:focus, &:active { @content; } };
@mixin hover { @include tablet-desktop { @include hoverall { @content; }; }; };
@mixin min($min) { @media(min-width:#{$min}px) { @content; } };
@mixin max($max) { @media(max-width:#{$max}px) { @content; } };
@mixin range($min: 0, $max: 1920) { @media (min-width:#{$min}px) and (max-width:#{$max}px) { @content } };
@function remove-nth($list, $index) { $result: null; @if type-of($index) !=number { @warn "$index: #{quote($index)} is not a number for `remove-nth`."; } @else if $index==0 { @warn "List index 0 must be a non-zero integer for `remove-nth`."; } @else if abs($index)>length($list) { @warn "List index is #{$index} but list is only #{length($list)} item long for `remove-nth`."; } @else { $result: (); $index: if($index < 0, length($list) + $index + 1, $index); @for $i from 1 through length($list) { @if $i !=$index { $result: append($result, nth($list, $i)); } } } @return $result; }
/* usage: @include transition(prop1, prop2, ..., 0.5s cubic-bezier(0.16, 0.85, 0.45, 1)); */
@mixin transition($args...) { $type: nth($args, length($args)); $props: remove-nth($args, length($args)); $result: (); @for $i from 1 through length($props) { $prop: nth($props, $i); $result: append($result, $prop); $result: append($result, $type); @if $i !=length($props) { $result: append($result, unquote($string: ",")); } } transition: $result; }
%btn {
    @include transition(background-color, color, border-color, 0.3s ease-in-out); display: block; border: 0 solid $primary-color;
    border-radius: .56vw; background-color: $primary-color; min-width: max-content; min-height: max-content; padding: 5px;
    text-decoration: none; font-family: $webfont; color: #fff; @include tablet-desktop { border-radius: .36vw; }
}
%btn-icon { position: relative; padding-right: 11.54vw; i { position: absolute; right: 3.92vw; } }
%btn-flex { display: flex; align-items: center; }
@mixin btn-hover { background-color: $secondary-color; color: #fff; border-color: $primary-color; }
%btn-primary-hover { @include btn-hover; }
.homepage .container, #main-content .container, .container, #sub-content { padding: 0 5vw; width: 100%; margin: 0 auto; max-width: 1530px; font-family: $webfont; @include tablet-desktop { padding: 0 15px; width: 90%; >div:not(#dnn_HeaderContactPane) { width: 100%; } } &, * { box-sizing: border-box; .coupon-wrap { &, & * { box-sizing: initial; } } } }
.text { display: block; &:nth-of-type(n+2) { margin-top: 1em; } }
.pc-header { &::before { background-color: darken($primary-color, $amount: 10%) !important; @include tablet { width: 100vw; left: -7vw; } } h1, h2, h3 { color: #fff; text-transform: uppercase; margin: 0; } } .atcsearchbody { min-width: 200px; }
.coupon-wrap { max-width: 630px; width: 100%; margin: 0 auto 0; @include tablet-desktop { width: 32.76vw; min-width: 330px; margin: 0; } .sliderImage .coupon-overlay { top: 0; bottom: 0; margin: auto 0; } }
.aqw-container { height: auto; min-width: 200px; margin: 0 auto 20px; border: 0 !important; background: unset; .aqw-header { display: none; } .aqw-steps { padding: 0; min-height: unset; .aqw-back-button { position: relative; line-height: normal; float: unset; } .aqw-h2 { margin: 0 auto 0 !important; width: 100%; padding: 0; font-family: $webfont; text-align: center; line-height: 1; span { color: #000 !important; } } .aqw-button-div { margin: 0 auto; width: 100%; box-sizing: border-box; border-radius: 0; .aqw-button-link.ndcustombutton2 { display: flex; align-items: center; justify-content: center; @extend %btn; margin: 0 auto; padding: 0; line-height: 1; &:hover { @extend %btn-primary-hover; } } } .aqw-smalltext { display: block; } } .aqw-breadcrumb-div { position: relative; margin: 10px auto; .aqw-breadcrumbs { padding-left: 15px; } } }
#find-tire-bar { @include phone { display: none; } #TireSizeFinder { display: flex; flex-wrap: wrap; #sizefinder-inputs { display: flex; align-items: center; flex-wrap: wrap; margin: 0; padding: 0; div { overflow: hidden; width: calc((100%/5) - 1vw); min-width: 120px; margin: 0 1vw 1vw 0; border-radius: 4px; border: 1px solid #000; select { width: 100% !important; border: 0; color: #6D6D6D; transition: none; border-radius: 0 !important; } } } #links { justify-content: flex-end; align-items: flex-start; .vlbCatalogBtn { @extend %btn; display: flex; align-items: center; justify-content: center; padding: 0; @include hover { @include btn-hover; } } } } }
#Body:not(.loggedIn) { #nd-actionbar { display: none; } } .PostalPanel, .GeoPanel { display: none !important; }
#contentheader { #dnn_dnnLogo_hypLogo { margin: 0; #dnn_dnnLogo_imgLogo { margin: 0; width: 100%; max-width: 100%; padding: 0; } } #dnn_HeaderContactPane { margin: 0; } }
@mixin make-responsive($class, $prop, $value) { #{$class} { #{$prop}: $value; @media (max-width:575.98px) { &-xs { #{$prop}: $value } } @media (min-width:576px) { &-sm { #{$prop}: $value } } @media (min-width:768px) { &-md, &-td { #{$prop}: $value } } @media (min-width:992px) { &-lg { #{$prop}: $value } } @media (min-width:1200px) { &-xl { #{$prop}: $value } } } }
/* Display */ @include make-responsive(".d-none", display, none); @include make-responsive(".d-flex", display, flex); @include make-responsive(".d-block, .break", display, block); @include make-responsive(".d-inline", display, inline); @include make-responsive(".d-inline-block, .d-iblock, .dib", display, inline-block);
/* Font Family */ @include make-responsive(".webfont, .f1, font-1", font-family, $webfont); @include make-responsive(".webfont2, .f2, font-2", font-family, $webfont2);
/* Font Style */ @include make-responsive(".i, .italic", font-style, italic); @include make-responsive(".ni, .nitalic, .no-italic", font-style, normal);
/* Font Weight */ @include make-responsive(".th, .thin", font-weight, 100); @include make-responsive(".el, .extralight, .extra-light", font-weight, 200); @include make-responsive(".li, .light", font-weight, 300); @include make-responsive(".re, .regular", font-weight, 400); @include make-responsive(".me, .medium", font-weight, 500); @include make-responsive(".se, .semibold", font-weight, 600); @include make-responsive(".bo, .b, .bold", font-weight, 700); @include make-responsive(".ex, .eb, .extrabold, extra-bold", font-weight, 800); @include make-responsive(".bl, .black", font-weight, 900);
/* Color */ @include make-responsive(".primary", color, $primary-color); @include make-responsive(".secondary", color, $secondary-color);
/* Default Navbar DESKTOP */
$nav-height: responsive-px(50, 78, 768, 1920); /* Height responsive */
$nav-font-size: responsive-px(16, 29, 768, 1920); /* font size responsive */
$nav-max-width: 100%; /* 100% to full width */
#Body { #nd-background { @include tablet-desktop { padding-top: $nav-height; } .nav-spacer { display: none; } } #contentnav { @include tablet-desktop { width: 100%; max-width: $nav-max-width; height: $nav-height; } #dnnMenu { &, .topLevel { height: 100%; } .topLevel>li.item { @include transition(background-color, border-color, color, 0.3s ease-in-out); &.selected>a { text-decoration: none; } a { @include transition(background-color, border-color, color, 0.3s ease-in-out); } >a { @include tablet-desktop { display: flex; justify-content: center; align-items: center; width: 100%; height: 100%; line-height: 1; font-size: $nav-font-size; } } @include hover { a { text-decoration: none; } &.haschild .subLevel { top: $nav-height; width: max-content; font-size: $nav-font-size; } } } } } }
/* Default Navbar MOBILE */ #Body { @include phone { #mobile-buttons { display: flex; align-items: center; justify-content: flex-end; height: 75px; .nd-mobile-button { & { padding: 0 1vw; } &.menu-phone, &.menu-location { display: block; padding-right: 2vw; } &.menu-menu { margin-right: auto; padding-left: 2vw; } } } .FindUsPanel .fa, .CallUsPanel .fa, .menu-quoting span.fas { display: none; } } }
/* styles navbar DESKTOP */
#nd-menubar {
    $back-color: #000;
    &, #contentnav { background-color: $back-color; }
    #contentnav .topLevel>li.item {
        @include tablet-desktop { border-right: responsive-px(1, 3, 768, 1920) solid #fff; &:last-child { border-right: 0; } }
        a { font-weight: 400; }
        >a { text-transform: capitalize; }
        .subLevel>ul {
            background-color: #000;
            a {
                font-weight: 600; color: #fff;
                @include tablet-desktop { border-color: #fff; border-width: 0; }
                @include hover { background-color: #fff; color: #000; }
            }
        }
        @include hover {
            >a { background-color: #fff; color: #000; }
        }
    }
}
/* styles navbar MOBILE */
#Body {
    .fa-phone { transform: rotateY(180deg); }
    @include phone {
        .mobileButtons { .mobileBG { background-color: $primary-color; opacity: 1; } .nd-mobile-button span { color: #fff; } }
        #contentnav { height: unset; }
    }
}
```