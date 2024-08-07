# webdevmnemonic
Mnemonic to help remembering stuff that's not semantic or just ambigious


## A to B

You know about `atob` & `btoa` functions in javascript, they don't make sense even though `A` should stand for ASCII and `b` to binary, and then you could razionalize that `b` might  be base64, but actually it's reverse.

* `atob` -> Decodes base64 
* `btoa` -> Encodes the string

Mnemonic to use: Beutiful to Awful
> You take your beutiful string and turn it to something aweful `btoa("beutiful string")`

source from [stackoverflow](https://stackoverflow.com/a/65207102) by user [Lunfel](https://stackoverflow.com/users/1114113/lunfel)


## Shift the array

`.shift` & `.unshift`

Mnemonic to use:
* .unshift - makes it bigger. Longer word than .shift
* .shift - makes it smaller. Shorter word than .unshift

source from [hacker news user da02 on Aug 7, 2013](https://news.ycombinator.com/item?id=6171882)


## What is origin?
When I was learning about CORS I didn't know what is origin, so I rememberd it as `PHP`. I was very proud on my "discovery" so it stuck for me.

Mnemonic to use: PHP
> Origin is combination of Protocol(scheme) Host Port -> PHP
source [ultrox](https://github.com/ultrox/)

## Sort the array

>if you're sorting an array in JS and keep forgetting how to write the compare functions (like I do), here's a mnemonic device:
source froM [David K](https://twitter.com/davidkpiano/status/1292237580780605440)

Mnemonic to use:
* (a, z) => a - z // ascending, like "a to z" or "from 1 to 100"
* (a, z) => z - a // descending, like "z to a" or "100 to 1"

<details>
<summary>Some more details</summary>

```js
var someItems = ["Feb", "Jan", "Apr", "Dec", "Oct"];

function sortMonths(a, b){
  var correctMonthsOrder = ["Jan", "Feb", "Mar", "Apr", "May", "Jun", "Jul", "Aug", "Sep", "Oct", "Nov", "Dec"];
  
  return correctMonthsOrder.indexOf(a) - correctMonthsOrder.indexOf(b);
}
```

to sort strings use [localeCompare](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/localeCompare) `a.localCompare(z)`
to sort arbitrary list like month, you'll need custom callback that associate items with numbers


someItems.sort(sortMonths);
src [Aphinya Dechalert](https://medium.com/madhash/demystifying-the-mysteries-of-sort-in-javascript-515ea5b48c7d)
</details>

## box-shadow

* Mnemonic to use: xy bs color
* How to read: xy bullshit color 
* Meaning: x y blur spread color



## ISO Profile (YYYY-MM-DD T HH:MM:SS Z)

### Problem
Remembering (mostly for europians) ISO profile YYYY-MM-DD is problematic, the rest make sense.

Profile used(formatting) of ISO date/time string uses RFC3339 to govern those rules


> **Note**
> You MY Day? :heart:

> **Note**
> You Are MY Day! :heart:

## NOTE:
This one is probably not needed, as logic RFC3339 was following is
to go from largest to smallest untit. Year being largest, ms being smallest


Sources:
* https://archive.ph/7cqtR#selection-735.22-735.23
* https://www.rfc-editor.org/rfc/rfc3339


## (oo) Git log diff between branches
### Problem:
You need to see what's new in origin/dev or origin/main compared to your current branch.

###Solution:
Use the following syntax: `git log HEAD..origin/main`

### Mnemonic:
The two dots ".." are like binoculars (oo). You (HEAD) are aiming to see what's on the target (origin/main).
