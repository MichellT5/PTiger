# Logobar
Here you can find most of tire logos available and some scss to make'em prettier. Hopefully you'll get same results.

### All same size
Preview:
![same size.jpg](brands-samesize.png)

```scss
#brands {
    display: flex; flex-wrap: wrap; justify-content: center; @include min(460) { .space { width: 100%; } }
    a {
        @include transition(transform, 0.3s ease-in-out); width: auto; justify-content: center; align-items: center; display: flex;
        img { object-fit: contain; object-position: center; margin: 0.5vw; width: 200px; height: 65px; }
        /* @include tablet-desktop { &:nth-of-type(-n+3) img { width: 26vw; height: unset; max-width: 450px; } } */
        &:hover { transform: scale(0.9); }
    }
}
```

### For Co-op uncomment the 6th line
![Co-op.jpg](brands-co-op.png)

### All available tirebrands
Note that first 6 logos have different `src` attribute and you'll have to upload them or change the `src` attribute, those are for Co-op required. The `<div class="space"></div>` is also for Co-op, they force a breakline.

```html
<div id="brands">
    <a href="/Shop-For-Tires/brands/Michelin" title="Michelin®">
        <img alt="Michelin® Tires" src="Skins/master/img/Michelin.png" />
    </a>
    <a href="/Shop-For-Tires/brands/BFGoodrich" title="BFGoodrich®">
        <img alt="BFGoodrich® Tires" src="Skins/master/img/BFGoodrich.png" />
    </a>
    <a href="/Shop-For-Tires/brands/Uniroyal" title="Uniroyal®">
        <img alt="Uniroyal® Tires" src="Skins/master/img/Uniroyal.png" />
    </a>
    <div class="space"></div>
    <a href="/Shop-For-Tires/brands/Bridgestone" title="Bridgestone®">
        <img alt="Bridgestone® Tires" src="Skins/master/img/Bridgestone.png" />
    </a>
    <a href="/Shop-For-Tires/brands/Firestone" title="Firestone®">
        <img alt="Firestone® Tires" src="Skins/master/img/Firestone.png" />
    </a>
    <a href="/Shop-For-Tires/brands/Fuzion" title="Fuzion®">
        <img alt="Fuzion® Tires" src="Skins/master/img/Fuzion.png" />
    </a>
    <div class="space"></div>
    <a href="/Shop-For-Tires/brands/Bandag" title="Bandag Tires®">
        <img alt="Bandag Tires" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_Bandag.png">
    </a>
    <a href="/Shop-For-Tires/brands/BFGoodrich" title="BFGoodrich Tires®">
        <img alt="BFGoodrich Tires®" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_BFGoodrich.png" />
    </a>
    <a href="/Shop-For-Tires/brands/Bridgestone" title="Bridgestone Tires®">
        <img alt="Bridgestone Tires®" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_Bridgestone.png" />
    </a>
    <a href="/Shop-For-Tires/brands/Capitol" title="Capitol Tires®">
        <img alt="Capitol Tires®" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_Capitol.png">
    </a>
    <a href="/Shop-For-Tires/brands/Carlisle Ag" title="Carlisle Ag Tires®">
        <img alt="Carlisle Ag Tires®" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_Carlisle.png">
    </a>
    <!-- <a href="/Shop-For-Tires/brands/Centennial" title="Centennial Tires®"> -->
        <!-- <img alt="Centennial Tires®" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_Centennial.png"> -->
    <!-- </a> -->
    <a href="/Shop-For-Tires/brands/Continental" title="Continental Tires®">
        <img alt="Continental Tires®" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_Continental.png">
    </a>
    <a href="/Shop-For-Tires/brands/Cooper" title="Cooper Tires®">
        <img alt="Cooper Tires" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_Cooper.png" />
    </a>
    <a href="/Shop-For-Tires/brands/Cordovan" title="Cordovan Tires®">
        <img alt="Cordovan Tires" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_Cordovan.png" />
    </a>
    <a href="/Shop-For-Tires/brands/Dayton" title="Dayton Tires®">
        <img alt="Dayton Tires" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_Dayton.png" />
    </a>
    <a href="/Shop-For-Tires/brands/Dean" title="Dean Tires®">
        <img alt="Dean Tires" src="https://a.nd-cdn.us/tire_brands/logos/logo_dean.gif" />
    </a>
    <a href="/Shop-For-Tires/brands/Delta" title="Delta Tires®">
        <img alt="Delta Tires" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_Delta.png" />
    </a>
    <!-- <a href="/Shop-For-Tires/brands/Diamondback" title="Diamondback Tires®"> -->
        <!-- <img alt="Diamondback Tires" src="//assets.netdrivenwebs.com/tire_brands/logos/png/Diamondback.png" /> -->
    <!-- </a> -->
    <a href="/Shop-For-Tires/brands/Dick Cepek" title="Dick Cepek Tires®">
        <img alt="Dick Cepek Tires" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_dick_cepek.png" />
    </a>
    <a href="/Shop-For-Tires/brands/Double Coin" title="Double Coin Tires®">
        <img alt="Double Coin Tires" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_doublecoin.png" />
    </a>
    <a href="/Shop-For-Tires/brands/Dunlop" title="Dunlop Tires®">
        <img alt="Dunlop Tires" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_Dunlop.png">
    </a>
    <a href="/Shop-For-Tires/brands/Eldorado" title="El Dorado Tires®">
        <img alt="El Dorado Tires" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_Eldorado.png">
    </a>
    <a href="/Shop-For-Tires/brands/Falken" title="Falken Tires®">
        <img alt="Falken Tires" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_Falken.png">
    </a>
    <a href="/Shop-For-Tires/brands/Firestone" title="Firestone Tires®">
        <img alt="Firestone Tires" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_Firestone.png" />
    </a>
    <a href="/Shop-For-Tires/brands/Fuzion" title="Fuzion Tires®">
        <img alt="Fuzion Tires" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_Fuzion.png" />
    </a>
    <a href="/Shop-For-Tires/brands/Galaxy Ag" title="Galaxy Ag Tires®">
        <img alt="Galaxy Ag Tires" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_Galaxy.png">
    </a>
    <a href="/Shop-For-Tires/brands/General" title="General Tires®">
        <img alt="General Tires" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_General.png">
    </a>
    <a href="/Shop-For-Tires/brands/Goodride" title="Goodride Tires®">
        <img alt="Goodride Tires" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_Goodride.png">
    </a>
    <a href="/Shop-For-Tires/brands/Goodyear" title="Goodyear Tires®">
        <img alt="Goodyear Tires" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_Goodyear.png">
    </a>
    <a href="/Shop-For-Tires/brands/Greenball" title="Greenball Tires®">
        <img alt="Greenball Tires" src="https://a.nd-cdn.us/tire_brands/logos/logo_Greenball.gif" />
    </a>
    <a href="/Shop-For-Tires/brands/GT Radial" title="GT Radial Tires®">
        <img alt="GT Radial Tires" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_GTRadial.png" />
    </a>
    <a href="/Shop-For-Tires/brands/Hankook" title="Hankook Tires®">
        <img alt="Hankook Tires" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_Hankook.png">
    </a>
    <a href="/Shop-For-Tires/brands/Hercules" title="Hercules Tires®">
        <img alt="Hercules Tires" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_Hercules.png">
    </a>
    <a href="/shop-for-tires/view/brand/b/106.aspx" title="Ironman Tires®">
        <img alt="Ironman Tires" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_Ironman.png">
    </a>
    <a href="/Shop-For-Tires/brands/Kelly" title="Kelly Tires®">
        <img alt="Kelly Tires" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_Kelly.png">
    </a>
    <a href="/Shop-For-Tires/brands/Kumho" title="Kumho Tires®">
        <img alt="Kumho Tires" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_Kumho.png">
    </a>
    <a href="/Shop-For-Tires/brands/Lemans" title="Lemans Tires®">
        <img alt="Lemans Tires®" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_Lemans.png" />
    </a>
    <a href="/Shop-For-Tires/brands/Lexani" title="Lexani Tires®">
        <img alt="Lexani Tires®" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_Lexani.png" />
    </a>
    <a href="/Shop-For-Tires/brands/Mastercraft" title="Mastercraft Tires®">
        <img alt="Mastercraft Tires" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_Mastercraft.png">
    </a>
    <a href="/Shop-For-Tires/brands/Maxxis" title="Maxxis Tires®">
        <img alt="Maxxis Tires" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_Maxxis.png">
    </a>
    <a href="/Shop-For-Tires/brands/Michelin" title="Michelin Tires®">
        <img alt="Michelin Tires" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_Michelin.png">
    </a>
    <a href="/Shop-For-Tires/brands/Mickey Thompson" title="Mickey Thompson®">
        <img alt="Mickey Thompson® Tires" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_Mickey_thompson.png" />
    </a>
    <a href="/Shop-For-Tires/brands/Milestar" title="Milestar Tires®">
        <img alt="Milestar Tires" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_Milestar.png">
    </a>
    <a href="/Shop-For-Tires/brands/Multi-Mile" title="Multi Mile Tires®">
        <img alt="Multi Mile Tires" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_MultiMile.png">
    </a>
    <!-- <a href="/Shop-For-Tires/brands/Negotiator" title="Negotiator Tires®"> -->
        <!-- <img alt="Negotiator Tires" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_Negotiator.png"> -->
    <!-- </a> -->
    <a href="/Shop-For-Tires/brands/Nexen" title="Nexen Tires®">
        <img alt="Nexen Tires" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_Nexen.png">
    </a>
    <a href="/Shop-For-Tires/brands/Nitto" title="Nitto Tires®">
        <img alt="Nitto Tires" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_Nitto.png">
    </a>
    <a href="/Shop-For-Tires/brands/Pirelli" title="Pirelli Tires®">
        <img alt="Pirelli Tires" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_Pirelli.png">
    </a>
    <a href="/Shop-For-Tires/brands/Primewell" title="Primewell Tires®">
        <img alt="Primewell Tires" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_Primewell.png">
    </a>
    <!-- <a href="/Shop-For-Tires/brands/Primex Ag" title="Primex Ag Tires®"> -->
        <!-- <img alt="Primex Ag Tires" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_Prime_ag.png"> -->
    <!-- </a> -->
    <a href="/Shop-For-Tires/brands/Pro Comp" title="Pro Comp Tires®">
        <img alt="Pro Comp Tires" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_Procomp.png">
    </a>
    <a href="/Shop-For-Tires/brands/Riken" title="Riken Tires®">
        <img alt="Riken Tires" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_Riken.png">
    </a>
    <!-- <a href="/Shop-For-Tires/brands/Roadlux" title="Roadlux Tires®"> -->
        <!-- <img alt="Roadlux Tires" src="//assets.netdrivenwebs.com/tire_brands/logos/png/Roadlux.png"> -->
    <!-- </a> -->
    <a href="/Shop-For-Tires/brands/Sailun" title="Sailun Tires®">
        <img alt="Sailun Tires" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_Sailun.png">
    </a>
    <!-- <a href="/Shop-For-Tires/brands/Samson Ag" title="Samson Ag Tires®"> -->
        <!-- <img alt="Samson Ag Tires" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_Samson.png"> -->
    <!-- </a> -->
    <a href="/Shop-For-Tires/brands/Starfire" title="Starfire Tires®">
        <img alt="Starfire Tires" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_Starfire.png">
    </a>
    <a href="/Shop-For-Tires/brands/Sumitomo" title="Sumitomo Tires®">
        <img alt="Sumitomo Tires" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_Sumitomo.png">
    </a>
    <a href="/Shop-For-Tires/brands/Summit" title="Summit Tires®">
        <img alt="Summit Tires" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_Summit.png">
    </a>
    <a href="/Shop-For-Tires/brands/Telstar" title="Telstar Tires®">
        <img alt="Telstar Tires" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_Telstar.png">
    </a>
    <a href="/Shop-For-Tires/brands/Titan Ag" title="Titan Ag Tires®">
        <img alt="Titan Ag Tires" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_Titan.png">
    </a>
    <a href="/Shop-For-Tires/brands/Toyo" title="Toyo Tires®">
        <img alt="Toyo Tires" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_Toyo.png">
    </a>
    <a href="/Shop-For-Tires/brands/Triangle" title="Triangle Tires®">
        <img alt="Triangle Tires" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_Triangle.png">
    </a>
    <a href="/Shop-For-Tires/brands/Uniroyal" title="Uniroyal Tires®">
        <img alt="Uniroyal Tires" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_Uniroyal.png">
    </a>
    <a href="/Shop-For-Tires/brands/Vogue" title="Vogue Tires®">
        <img alt="Vogue Tires" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_Vogue.png">
    </a>
    <a href="/Shop-For-Tires/brands/Yokohama" title="Yokohama®">
        <img alt="Yokohama® Tires" src="//assets.netdrivenwebs.com/tire_brands/logos/png/logo_yokohama.png">
    </a>
</div>
```

### Contributions
* Souce Code by Daniel Aguirre