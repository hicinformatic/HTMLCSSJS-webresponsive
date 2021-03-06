
# wr-easy
## La librairie CSS webresponsive sans surcouche javascript.

wr-easy est une librairie CSS3 qui ne nécessite pas de surcouche javascript.
En revanche elle n'apporte aucun style de base pour laisser libre choix aux webdesigner.
Elle n'a que pour seul but, simplifier au maximum la gestion webresponsive d'un site internet.

Vous pouvez voir son utilisation ici:
http://onestaufond.fr/index.html

## Quelques exemples:

###### Un simple Menu responsive
```
<!--
Couleur du streak (bouton déroulant) en mode responsive:
nav>label>span>span:nth-child(even){ background-color: #******; }

Modification de la taille du menu déroulant en mode responsive:
style="height: 45px;"
-->
<nav>
    <input id="discoverMenu" class="wr-display-none" type="checkbox">
    <label for="discoverMenu" class="wr-menudiscover wr-only-sm wr-only-md wr-txt-right" style="height: 45px;">
        <span class="wr-streak">
            <span></span>
            <span></span>
            <span></span>
            <span></span>
            <span></span>
            <span></span>
            <span></span>
        </span>
    </label>
    <div class="wr-block wr-inline-lg wr-txt-center">
        <a href="#">Menu 1</a><!--
     --><a href="#">Menu 2</a><!--
     --><a href="#">Menu 3</a>
    </div>
</nav>
```

###### Une grille automatique de 1 à 10 colonnes
```
<div class="wr-inline">
   <div>Col1</div><!--
--><div>Col2</div>
            [...]
--><div>Col9</div>
--><div>Col0</div>
</div>
```

###### Une grille sur mesure de 1% à 100%
```
<div class="wr-fill">
   <div class="wr-width10">10%</div><!--
--><div class="wr-width50">50%</div><!--
--><div class="wr-width25">25%</div><!--
--><div class="wr-width15">15%</div>
</div>
```

###### Gestion webresponsive
| Taile | Description | Informations |
| --- | --- | --- |
| lg | large > | > 993px (En général des laptops) |
| md | medium | > 769px et < 993px (En général des tablets) |
| sm | small | < 769 px (En général des smartphones) |

```
<!-- All size -->
<div class="wr-fill"></div>
<div class="wr-inline"></div>

<!-- Large -->
<div class="wr-fill-lg"></div>
<div class="wr-inline-lg"></div>

<!-- Medium -->
<div class="wr-fill-md"></div>
<div class="wr-inline-md"></div>

<!-- Small -->
<div class="wr-fill-sm"></div>
<div class="wr-inline-sm"></div>

<!-- Association Large & Medium-->
<div class="wr-fill-lg wr-fill-md"></div>
<div class="wr-inline-lg wr-inline-md"></div>

<!-- Association Medium et Small -->
<div class="wr-fill-md wr-fill-sm"></div>
<div class="wr-inline-md wr-inline-sm"></div>
```

###### Message d'alerte (Bouton de suppression du message disponible)
| Type | Description |
| --- | --- | --- |
| wr-info | Informations |
| wr-success | Réussite |
| wr-warning | Attention |
| wr-danger | Danger |
```
<div>
    <input class="wr-untoggle" id="bulle-info" type="checkbox">
    <div class="wr-success">
        <label class="wr-block wr-txt-right wr-sym-cross" for="bulle-info"></label>
        <p><span class="wr-sym-warning"> Success</span> </p>
    </div>
    <div class="wr-break10"></div>
</div>
```

###### Tabs (sans javascript a hauteur dynamique)
```
<div lass="wr-tabs">
    <input class="wr-tab" type="radio" id="s1" name="s" checked/>
    <input class="wr-tab" type="radio" id="s2" name="s"/>
    <input class="wr-tab" type="radio" id="s9" name="s"/>
    <input class="wr-tab" type="radio" id="s10" name="s"/>
    <div class="wr-tab wr-inline">
        <label for="s1">Tab1</label><!--
     --><label for="s2">Tab2</label><!--
            [ .. ]
     --><label for="s9">Tab9</label><!--
     --><label for="s10">Tab10</label>
    </div>
    <div class="wr-tabcontent">
        <div>Tab1</div>
        <div>Tab2</div>
        [ ... ]
        <div>Tab9</div>
        <div>Tab10</div>
    </div>
</div>
```

