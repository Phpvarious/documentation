
<a href="{{site.url}}/documentation">Accueil</a> --> <a href="{{site.url}}/documentation/{{site.widget}}">Widget</a> --> <a href="{{site.url}}/documentation/{{site.widget}}/fr_FR/info/numeric">Info / Numérique</a> --> Countdown

------------

# Widget [Countdown] ![Generic badge](https://img.shields.io/badge/Version-4.4%20%7C%204.5%20Full%20JS-green.svg)

<img src="images/capture1.gif" alt="HygroThermographe_svg" />

> [!WARNING]
> test
>
> test 2

<div class="alert alert-warning"><i class="fas fa-exclamation-circle"></i> <strong>info : </strong> Ce widget a pour but d'afficher simplement un compte a rebours en fonction de la valeur (timestamp) de la commande.</div>

## Télécharger la source
> - <a href="{{site.url_git}}/WIDGET_cmd.info.numeric.countdown" target="_blank">Télécharger les sources du Widget pour le Core V4</a>

### Version dashboard

- Déposer le fichier <b>cmd.info.numeric.compteur1.html</b> dans le dossier <b>/html/data/customTemplates/dashboard/</b>

  <img src="images/install1.png" alt="Téléchargement du widget" />

## Installation
- Créer un nouveau virtuel.
- Ajouter une commande info / numérique puis lui appliquer le widget `Countdown`.

<img src="images/virtual1.png" class="border" alt="Virtuel 1" />

### Ajout des boutons

####  Bouton reset
Dans ce même équipement ajoutez une commande action/défaut.<br>

<img src="images/virtual2.png" class="border" alt="Virtuel 2" />


- <i>Nom information : nom de la commande info/numerique qui contient le widget (`Décompte` pour mon exemple)</i>
- <i>Valeur : 0</i>

####  Bouton +
Dans ce même équipement ajoutez une commande action/défaut (Ex : `+10`)<br>

<img src="images/virtual3.png" class="border" alt="Virtuel 3" />

- <i>Nom information : nom de la commande info/numerique qui contient le widget (`Décompte` pour mon exemple)</i>
- <i>Valeur : `(#timestamp# <= #[Décompte]#) ? (#[Décompte]# + 10) : (#timestamp# + 10)`</i>
  - `#[Décompte]#` a remplacer par le nom complet de votre commande (Ex : `#[Objet][eqLogic][Décompte]#`)

Pour un bouton +60 (+1mn), répéter cette même étape, modifier simplement la valeur du champs `valeur`.<br>
Ex : `(#timestamp# <= #[Décompte]#) ? (#[Décompte]# + 60) : (#timestamp# + 60)`

####  Bouton -
Toujours dans ce même équipement ajoutez une commande action/défaut.  (Ex : `-10`)<br>

<img src="images/virtual4.png" class="border" alt="Virtuel 4" />

- <i>Nom information : nom de la commande info/numerique qui contient le widget (`Décompte` pour mon exemple)</i>
- <i>Valeur :</i> `(#timestamp# >= #[Décompte]# - 10) ? 0 : (#[Décompte]# - 10)`
  - `#[Décompte]#` a remplacer par le nom complet de votre commande (Ex : `#[Objet][eqLogic][Décompte]#`)


Pour un bouton -60 (-1mn), répéter cette même étape, modifier simplement le champs `valeur`.<br>
Ex : `(#timestamp# >= #[Décompte]# - 60) ? 0 : (#[Décompte]# - 60)`

## Paramètres optionnels

<img src="images/parametres1.png" class="border" alt="Paramètres" />


## Changelog

<a href="./changelog">Changelog</a>

## Aide
> - [Comment récupérer les sources ?]({{site.url}}/documentation/{{site.help}}/fr_FR/download)
> - [Comment ajouter des paramètres ?]({{site.url}}/documentation/{{site.help}}/fr_FR/application)

-------------------

<a href="{{site.url}}/documentation">Accueil</a> --> <a href="{{site.url}}/documentation/{{site.widget}}">Widget</a> --> <a href="{{site.url}}/documentation/{{site.widget}}/fr_FR/info/numeric">Info / Numérique</a> --> Countdown