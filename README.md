

# MTG Tooltip Js



A simple vanilla javascript plugin to create images tooltips for magic the gathering cards. No dependencies, no extra css, just a .js file and little bit of html.

You can check it working live [here](https://giventofly.github.io/MTG-Tooltip-Js/), along with some **examples** of usage and a "nicier" page. Seriously, [check it](https://giventofly.github.io/MTG-Tooltip-Js/) with examples its way better

What advantages do i have over ([Inline mtg](https://gist.github.com/NickolasReynolds/9306194) - my inspiration/basepoint) the previous one?

* No libraries needed, just good old plain javascript
* lazyload tooltip images (performance and banwith is important, no?)
* Low size (13kb and 7Kb minified).
* You can select defaults sets for shocklands, painlands, fetchlands, and basics (more can be added, make a pull request or ask me)
* option to now load/start on mobile (you don't have a mouse to mover over the images/name, do you?)
* option to remove elements created and rescan the page
* check them all...

  **

## API

    mtgtooltip.start(); //starts, only used to rescan the page and load new items or when start is set to false
    mtgtooltip.kill() // to remove all instances of the tooltip and addEventListeners.


| option | default | options | description |
|--|--|--|--|
| element |body|String|The element you want to append the tooltips to (need to have position defined) |
| lazyload |true|bool (true/false)|If you want to lazyload the tooltip images.|
|fadetime|300|integer (ms)|If you want the tooltip to fade in X ms|
 |opacity|1|float [0,1]|The opacity for the tooltip to have.|
 |log|false|bool (true/false)|verbose to the console what's going on.|
|start|true|bool (true/false)|Start mtgtooltip on the instance creation.|
|wrap_in|-|String|inicial wrap in case for some special css/js reasons for the tooltip|
|wrap_out|-|String|final wrap in case for some special css/js reasons for the tooltip|
|specialImage|-|String|link to use costumized image on request (for the data-specialimage attribute)|
|mobile|true|bool (true/false)|Don't start the mtgtooltip on mobile/tablet devices.|
|basiclands|ust|String (ust,unh,ugl)|unstable, unhinged and unglued respectively|
|shocklands|exp|String (old,new,exp)|old: (dissension,ravnica), new: gatecrash, return to ravnica, exp: expeditions|
|fetchlands|exp|String (old,new,exp)|old: zendikar, onslaught, new: modern master 3, khans of tarkir, exp: expeditions|
|painlands|exp|String (old,new,exp)|old: ice age, apocalypse, new: magic origins, exp: tenth edition, sixth edition|

Normal usage:

    <span class='mtgtooltip'>Tarmogoyf</span>

Set name:
```
<span class='mtgtooltip' data-name="Bloodbraid Elf">i'm freeeee</span>
```
Set edition:
```
<span class='mtgtooltip' data-set='ZEN'>Arid Mesa</span>
```
Set multiverseid:
```
<span class='mtgtooltip' data-multiverseid='4562'>Tarmogoyf</span>
```
Specific image usage
```
<span class='mtgtooltip' data-specialimg="myimage.jpg">My altered Baneslayer Angel</span>
```

## Quick Start:

```
<script src='https://raw.githubusercontent.com/giventofly/MTG-Tooltip-Js/dist/mtgtooltip.js'></script>
```

```
document.addEventListener('DOMContentLoaded', function () {
        tooltips = new mtgTooltip();
    });

```


## Upgrades? Suggestions?

Open a issue/pull request or contact me.

## Want to make me be able to buy some cards?

 [paypal.me](https://www.paypal.me/heyzeto)!! **Thank you.**


