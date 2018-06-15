# Documentation

## Convention BEM

* B => Black
* E => Element
* M => Modifier

```html
<ul class="mainList mainList--xmas">
<li class="mainList_items">
  <a class="mainList_itemLink mainList_itemLink--isActive" href="./home">Home</a>
</li>
<li class="mainList_items">
  <a class="mainList_itemLink" href="./about">About</a>
</li>
<li class="mainList_items">
  <a class="mainList_itemLink" href="./works">Works</a>
</li>

</ul>

```

```css

.mainList{
  display: flex;
  justify-content: space-between;
  &--xmas{
    background: green;
  }
  &__item{
    list-style: none;
  }
  &__itemLink{
    color: red;
  &--isActive{
    color: white;
  }
  }
}
```

## Pseudos Attributs

Les pseudos attributs `before` et `after` permettent de crée des noeuds HTML en CSS,
Ils sont essentiellement utilisés pour ajouter des ornements, des décorations ... On peut bien entendu faire animation avec, les positionner pr rapport à leur parent (relative / absolute). **Ils doivent obligatoirement avoir un `content:``**

```HTML
<section class="cover">
  <h1 class="cover_mainTitle">Présentation des pseudo-attributs</h1>
</section>

```

```CSS
.cover{
  background:red;
  padding:20px;
  &__mainTitle{
    text-align:center;
    font-size:24px;
    color:green;
    &::before,
    &::after {
      content:'';
      posotion:absolute;
      display: block;
      width: 50px;
      height: 50px;
      background: green;
    }::before{
      left:0;
    }
  }::after{
    right:0;
  }
}
```

## REM, EM, X, VW Sizing

### X

### EM
* relative a la taille de son parent direct.

```css
.cover{
  font-size: 100%;
  &__mainTitle{
    font-size:.8em;
  }
}

```

### REM

* Le REM est basé sur la taille de racine (soit la balise <html>) qui, par défaut ) ine valeur de 16px. Afin d'éviter tout calcul; il est nécessaire de l'écraser donnant une base de 10px soit 62,5%.
* Le REM est intéressant à utiliser si les média-queries employées sont en rem également. Cela vous permettra de garder des proportions égles lorsqu'on va redimensionner la page.
* Ses propotions seront également gardées quand l'utilisateur zoomera dans votre page.


```css
html{
  font-size: 62.5%;
}

```

### VW(idth) / VH(eight)

* Unités relatives ) la taille de votre écran (peu importe le device)
* Attention au VH et à son contenu. 100vh == 100vh quoi qu'il arrive.
* VW : très utile pour les interface fluides.

### Les utilies :



### Les Flexbox Grid

* Les modificateurs réactifs permettent de spécifier différentes tailles de colonnes, décalages, alignement et distribution aux largeurs de la fenêtre xs, sm, md & lg

* NOTE : Jamais modifier le padding & margin des colonnes


### Les liens utiles

*  NOTE : http://flexboxgrid.com/
*  NOTE : https://github.com/h5bp/Front-end-Developer-Interview-Questions Q&A qu'on peu avoir en entretien
*  NOTE : http://cssnext.io/  FUTUR DU CSS Actuellement CSS3
*  NOTE : https://caniuse.com/ c'est compatible ou pô
