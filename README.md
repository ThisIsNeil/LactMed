# LactMed


<div align="center">

  <a href="http://wikimedicine.ir/">![Static Badge](https://img.shields.io/badge/Under-Wikimedicine-green?color=%23008000)</a>
  <a href="https://creativecommons.org/licenses/by-nc-sa/4.0/">![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC_BY--NC--SA_4.0-lightgrey.svg)</a>  </br>
  <a href="">![Github Created At](https://img.shields.io/github/created-at/ThisIsNeil/LactMed?style=plastic)</a>
  <a href="">![GitHub last commit](https://img.shields.io/github/last-commit/ThisIsNeil/LactMed?style=plastic&color=blue)</a>

</div>

Searchable index of drug safety during pregnancy and lactation.
## Tooltips

There are two different ways tooltips were used in this work:

1. Badges
2. docile tooltip

### Badges:

Badge refers to the icons of FDA (US Agency) and TGA (Australian Agency) etc. which are responsible for food and drug safety respectively in the aforementioned countries.

there's three part to adding badges to this work:

1. the badge.css file
2. badge icons
3. the code added to each drug individually

since there's no consistency between each drug's recommendation,I've chosen to write the whole "hover box" individually for each drug.

the badge.css file is located at /css

badges are accessible from /res/badges

and the example code which should replace <td></td> tags is as follow:

```
<td class="CellWithComment">
Name of drug
<span style="text-align: start" class="CellComment">
	<a class="badgeheaderdrugs">Drugs.com</a><a class="badgeheaderrest"> recommendation:<br style="line-height: 30px"></a>
	<a class="badgecontent">Pregnancy Category:&ensp; &ensp;<img style="vertical-align:middle" alt="FDA Group A" src="/res/badges/fda/fda_a.svg"> <img style="vertical-align:middle" alt="FDA Group A" src="/res/badges/fda/fda_a.svg"><br style="line-height: 40px">Breastfeeding Category:<img style="vertical-align:middle" alt="FDA Group A" src="/res/badges/fda/fda_a.svg"> <img style="vertical-align:middle" alt="FDA Group A" src="/res/badges/fda/fda_a.svg"></a>
<i></i>
</span>
</td>
```

**<!img> codes for badges:**
> |Badge                                | (Delete the "!" before the <!img>                          |
> | ----------------------------------- | ---------------------------------------------------------- |
> | ![FDA A](/res/badges/fda/fda_a.svg) | <!img alt="FDA Group A" src="/res/badges/fda/fda_a.svg"> |
> | ![FDA B](/res/badges/fda/fda_b.svg) | <!img alt="FDA Group B" src="/res/badges/fda/fda_b.svg"> |
> | ![FDA C](/res/badges/fda/fda_c.svg) | <!img alt="FDA Group C" src="/res/badges/fda/fda_c.svg"> |
> | ![FDA D](/res/badges/fda/fda_d.svg) | <!img alt="FDA Group D" src="/res/badges/fda/fda_d.svg"> |
> | ![FDA X](/res/badges/fda/fda_x.svg) | <!img alt="FDA Group X" src="/res/badges/fda/fda_x.svg"> |
> |                                     |                                                           |
> |                                     |                                                           |
> |                                     |                                                           |
> |                                     |                                                           |
> |                                     |                                                           |
>
> 
>
> 

**Badge color scheme:**

- FDA:
  - ​	A:#51d91e
  - ​	B:#f4ff00
  - ​	C:#FFC300 
  - ​	D:#ff6100
  - ​	X:#ff0000

-----------

### Docile tooltip:

while creating badges I undrestood I couldn't use <div> inside <td></td> which killed the whole badge section at first and I kept making different adjustments and experiment with what could be done and created the "docile tooltip". 

docile tooltip has a different style to it and was kept since it could prove useful one day.as of now there's no implementation of docile tooltip inside the index file but the css which is located at /css/docile_tooltip.css is loaded automatically.

the website I used for implementing docile tooltip can be found at https://freefrontend.com/css-tooltips/ and was created by R. Schnetzinger and further edited to look something like this:

```
<div class="example-elements">
<a data-tooltip="text inside the tooltip" data-tooltip-location="right">the hoverable text</a>
</div>
```

- this code can be used be between the <td> </td> tags which I never understood why this works and my initial badges didn't.

- it is only capable of showing text and no images.

- there's other directions for the tooltip that I didn't remove since it may be used someday.

  


-------------
## Fun stuff

Easter Egg: putting this code inside the css of the tooltip causes it to show at an angle:

```
    transform:translate(50%,-50%) rotate(-45deg);
    background-color:#EEEEEE;
    box-shadow:0 1px 8px rgba(0,0,0,0.5);
```
-----------
<a href="https://github.com/micahlt/renart">![Static Badge](https://img.shields.io/badge/Based_on-micahlt/renart-green?color=%236495ED)</a> </br>
License: This work is licensed under Attribution-NonCommercial-ShareAlike 4.0 International. To view a copy of this license, visit <a href = "http://creativecommons.org/licenses/by-nc-sa/4.0/">http://creativecommons.org/licenses/by-nc-sa/4.0/</a>
