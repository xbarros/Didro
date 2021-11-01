
 <!DOCTYPE html>
<html>
<head>
<style>
.button {
  background-color: white;
  border: 1px solid;
  border-color: black;
  font-family:"Lato",sans-serif;
  font-weight:350;
  color: black!important;
  padding: 10px 10px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  margin: 4px 2px;
  cursor: pointer;
}
.button:hover {
  text-decoration:none;
  background-color: black; 
  color: white!important;
}
.round-button {
    display:block;
    width:100px;
    height:100px;
    line-height:17px;
    border:0px ;
    border-radius: 50%;
    color:#6069db;
    text-align:center;
    text-decoration:none;
    display: table-cell;
    vertical-align: middle;
    background: #6069db;
    box-shadow: 0 0 0px gray;
    font-size:14px;
    font-weight:bold;
    }

</style>
</head>
</html>

<div align="right"> 
    <a href="http://files.edunumsec2.ch/enjeux-sociaux/economie-numerique.pdf" class="round-button">
         <font color=white id="demo">Voir <br>dossier</font>
    </a>
</div>

# IA et enjeux de l'automatisation

<br>

Ce dossier aborde le vaste sujet que forment l’intelligence artificielle (IA) et l’automatisation. Qu’est-ce que l’IA, d’où vient-elle et comment impose-t-elle une certaine vision du monde ? Quelles sont les opportunités, les craintes et les problèmes propres aux applications de l’IA ? Comment réguler les usages de ces nouvelles technologies ?

## Objectifs

* Comprendre le contexte d’émergence de l’intelligence artificielle
* Différencier l’IA symbolique et connexionniste
* Connaître les forces et les faiblesses de l’IA
* Comprendre les enjeux relatifs à la délégation des prises de décisions 
* Prendre conscience des différentes manières de réguler les pratiques liées à l’IA


## Introduction

<br>

La quête d’une forme d’intelligence artificielle n’est pas nouvelle et apparait dans la littérature dès 1818 avec le fameux roman « Frankenstein» de Mary Shelley. Plus tard, la science-fiction en fera également un thème central et récurrent, des premiers robots rebelles de la pièce R.U.R. (Čapek, 1920) à la voix artificielle de Her du film homonyme (Spike Jonze, 2013). Ces personnages sont des exemples d’**intelligence artificielle forte**, ils sont autonomes et dotés d’une conscience. L’impact des histoires et des images issus de la science-fiction sont perceptibles dans certaines représentations, fantasmes et inquiétudes suscitées par l’IA. Mais les récits fictifs qui mobilisent diverses formes d’IA n’ont pas la prétention de prédire l’avenir. De plus, les techniques actuelles se limitent à de l’**intelligence artificielle faible**, centrées sur une tâche précise. La lecture des récits de science-fiction permet surtout d’identifier des problématiques centrales concernant les aspects philosophiques, sociaux ou juridiques autours de l’IA. Le retour en force de l’IA observé depuis le début des années 2010 nous amènent à réfléchir à certaines questions longtemps restreintes au monde de la fiction. Quelle place accorde-t-on à l’IA et à ses technologies ? Sont-elles pensées en opposition ou au contraire, avec l’intelligence humaine ? Qui est responsable en cas de problème généré par une machine ?

Pour apporter des pistes de réflexion, un rappel du contexte d’émergence de l’IA est proposé avant de présenter trois enjeux contemporains propres à ses utilisations.



<div align="left"; style="font-size:20px ;color:rgb(0, 0, 0); font-family:helvetica">
  <b>🕶 Une vision de l’intelligence</b>
</div>

<br>

L’émergence des premières techniques dites d’intelligence artificielle s’inscrit dans le courant de pensée de la cybernétique, fondé par le mathématicien Norbert Wiener à la fin des années 1940 aux États-Unis. Ce mouvement interdisciplinaire considère que tous les systèmes vivants (humains et animaux) et matériel (machines) sont régulés par une loi générale basée sur des boucles de rétroaction ou feedback. Cette conjecture permet de placer les humains et les machines sur un pied d’égalité quant à leur fonctionnement. Elle promeut une vision formaliste et donc simplificatrice du fonctionnement du vivant. Bien que réductrice, cette approche permettra notamment d’envisager les premières théories concernant l’intelligence artificielle basée sur le raisonnement humain.

L’engouement autour de la cybernétique s’essouffle à la moitié des années 1960, mais son influence reste aujourd’hui encore perceptible dans de nombreux domaines scientifiques tels que les sciences cognitives, l’informatique et bien sur les recherches en IA.

**« Les machines peuvent-elles penser ? »**

C’est la question que pose le mathématicien britannique Alan Turing dans un célèbre article publié en 1950. Pour y répondre, il propose le « jeu de l’imitation », également connu sous le nom de « Test de Turing ». L’expérience se résume comme suit : Un être humain (A) est mis en communication via un clavier et un écran, avec deux entités qu’il ne voit pas et dont il ignore la nature ; d’un côté, se trouve un ordinateur (B), de l’autre, un humain (C). Si, au bout de 5 minutes de conversation, l’être humain (A) n’est pas capable de savoir qui de (B) et (C) est l’ordinateur, ce dernier passe le test.

Le jeu de l’imitation est avant tout un exemple théorique. La puissance des machines des années 1950 ne permet pas d’envisager l’assimilation des questions et encore moins la formulation de réponses adaptées. Aujourd’hui, les agents conversationnels ou chat bots sont ce qui se rapprochent le plus de l’ordinateur du jeu de l’imitation. Leurs performances actuelles demeurent relativement faibles et sont encore loin de créer la confusion pour les utilisateurs.

Au-delà de la pertinence du jeu de l’imitation, sa conceptualisation permet de comprendre comment Turing concevait la pensée. Pour lui, il s’agit de capacités cognitives, c’est-à-dire d’un ensemble de facultés qui permettent d’apprendre, d’organiser et d’utiliser les connaissances. En considérant que la pensée peut être réduite à un ensemble de facultés définies (entre autres la perception, la mémoire et le langage), il devient également possible d’envisager de les reproduire de manière artificielle. C’est sur ce principe, inspiré de la cybernétique, que se baseront les premières recherches dans le domaine, quelques années plus tard. Cette approche très rationnelle de la pensée permet de placer l’intelligence humaine et l’intelligence artificielle au même niveau afin de les mettre en opposition. Le rapport de force entre l’être humain et la machine instauré par Turing exercera une influence certaine dans l’histoire. Cette opposition servira de point de repère pour évaluer l’efficacité de différents systèmes d’IA face à l’intelligence humaine.

**Création d’un domaine scientifique**

Le terme intelligence artificielle ou plutôt artificial intelligence en anglais, apparaissent pour la première fois en 1955, aux États-Unis. Quatre scientifiques formés en mathématique et en neurologie organisent une conférence d’été au Dartmouth College, afin de discuter et de réfléchir aux questions de programmation et de langage des ordinateurs, de réseaux de neurones, de puissance de calcul et d’auto-apprentissage. Mises ensemble, ces disciplines forment un nouveau domaine appelé intelligence artificielle.
Dans leur [proposition de projet](http://jmc.stanford.edu/articles/dartmouth/dartmouth.pdf) les auteurs expliquent leur approche de la manière suivante :

*« L’étude devra se dérouler sur la base de la conjecture que chaque aspect de l’apprentissage ou toute autre caractéristique de l’intelligence peut, en principe, être décrit avec une telle précision qu’une machine peut être conçue pour la simuler »*

L’un des but motivant les premières recherches en IA est explicitement de reproduire l’intelligence humaine. Comme Turing avant eux, les pionniers de l’IA partent du principe que le fonctionnement du raisonnement humain est suffisamment compris pour être modélisé. Certes, cette approche permet d’ouvrir la voie dans certains domaines bien précis. Cependant, l’intelligence humaine ne se limitent pas à un processus logique, mesurable et individuel contrairement aux idées des pionniers de l’IA. Cette conception est en fait porteuse d’un paradoxe : pour pouvoir modéliser et reproduire artificiellement l’intelligence, elle est réduite à des fonctions définies. Or, les notions d’intelligence sociale, émotionnelle ou créative sont exclues du problème. La notion du corps est également totalement absente de ces considérations.

**Courants symbolique et connexionniste**

Trouver une définition générale de l’IA est un exercice difficile car il s’agit en fait d’un ensemble de technologies particulières. Historiquement, on différencie principalement deux approches, avec d’un côté l’IA symbolique qui vise à reproduire le raisonnement humain sous la forme de règles statiques pour l’intégrer à des machines. C’est sur ce principe que reposent l’ordinateur du jeu de l’imitation et les systèmes experts. De l’autre, l’IA connexionniste est un ensemble de techniques d’apprentissage basées sur de grands volumes de données. Elle comprend l’apprentissage automatique ou machine learning et l’apprentissage profond ou deep learning. Cette dernière utilise des modèles de réseaux de neurones, superposés en plusieurs couches pour établir des règles complexes de manière autonome. 

Les techniques d’IA sont principalement utilisées à des fins prédictives. À partir d’importants volumes d’informations connues, des modèles statistiques sont mis au point et servent ensuite à prédire des faits ou des comportements. 


<div align="left"; style="font-size:20px ;color:rgb(0, 0, 0); font-family:helvetica">
  <b>L'IA, avec ou contre nous?</b>
</div>

La force de prédiction des intelligences artificielles n’a cessé d’augmenté depuis son émergence. En 1997, la victoire du superordinateur Deep Blue (IBM) face au grand maître d’échec Garry Kasporov marque un tournant dans l’histoire opposant l’humain à la machine. Lors de sa victoire, Deep Blue calcule environ 200 millions de possibilités par seconde ce qui correspond à l’anticipation de 12 coups. Kasparov est capable d’anticiper au mieux les 10 prochains coups. Mais cet exploit a également nécessité d’importants moyens humains. Les ingénieurs d’IBM ont travaillé plus de 10 ans pour développer «Deep Blue». Ce sont également des données produites par de grands joueurs qui ont servi à entrainer la machine.  

En 2015, l’histoire de l’IA est à nouveau marquée par une victoire de la machine sur l’être humain. Le programme informatique AlphaGo (développée par la société britannique Deep Mind, rachetée par Google en 2014) bat un joueur professionnel lors d’une partie du traditionnel jeu de Go. L’exploit réside surtout dans le cheminement emprunté pour parvenir à cette victoire. Le jeu de Go est bien plus complexe que les échecs et les possibilités sont trop nombreuses pour être listées et apprises à une machine. Une combinaison d’apprentissage supervisé considérant des parties jouées par des humains et d’apprentissage profond uniquement basé sur l’expérience de la machine va permettre à AlphaGo de déduire les coups optimaux et de battre pour la première fois de l’histoire un joueur professionnel. La dernière version du programme baptisée AlphaGo Zero est parvenue à battre n’importe quel joueur humain ainsi qu’AlphaGo lui-même, en apprenant uniquement de sa propre expérience. Le programme est ainsi devenu imbattable. 

Ces exemples montrent que les technologies de l’IA peuvent s’avérer plus performantes que l’être humain dans des situations précises. Ces domaines de performance correspondent à des environnements fermés, où le but est fixé à l’avance. C’est le cas du jeu d’échec et du jeu de Go. La logique d’opposition est également privilégiée par le contexte du jeu et du calcul de la performance de la machine contre le joueur. Mais cette logique élude tout le travail que l’humain a consacré au développement de ses programmes, sans lequel l’exploit ne peut pas avoir lieu. 

<div align="left"; style="font-size:20px ;color:rgb(0, 0, 0); font-family:helvetica">
  <b>⚒ Le travail au défi de l'automatisation</b>
</div>

<br>
La logique de l’opposition entre l’être humain et la machine, souvent thématisé en science-fiction et reprise dans la présentation des victoires de Deep Blue et AlphaGo, est à l’origine d’une crainte quant au remplacement des travailleurs et travailleuses humains par des systèmes automatisés. En 2013, une étude menée par des chercheurs de l’Université d’Oxford conclut que 47% des emplois ont une forte probabilité de disparaître compte tenu des avancées dans le domaine de l’apprentissage automatique. Des erreurs méthodologiques sont rapidement identifiées et discrédites les résultats de la recherche. Le sociologue Antonio Casilli (EHESS) souligne que les auteurs de l’étude d’Oxford ne prennent pas en compte les résistances sociales souvent engendrées par la suppression de postes de travail.

<div align="left"; style="font-size:20px ;color:rgb(0, 0, 0); font-family:helvetica">
  <b>Réguler</b>
</div>

À la suite des diverses controverses engendrées par les biais racistes des IA, certaines grandes entreprises comme Google, Microsoft ou IBM ont mis en place des comités d’éthique. Plusieurs projets en cours ont ainsi été suspendus ou abandonnés en raison du risque de perpétuer des pratiques discriminatoires. Il s’agit dans ce cas d’une forme de gouvernance interne aux entreprises qui n'est pas contraignante. 

Une autre manière d’appréhender les risques liés à l’IA est de légiférer sur ses usages. Aux [États-Unis](https://www.ncsl.org/research/telecommunications-and-information-technology/2020-legislation-related-to-artificial-intelligence.aspx), leader mondial dans le domaine, seuls quatre états avaient adopté une forme de regulation relative à l'IA en 2021. En Europe, la Commission Européenne a proposé en avril 2021 « [un ensemble d’actions visant à stimuler l’excellence dans le domaine de l’IA, ainsi que des règles destinées à garantir la fiabilité de cette technologie](https://ec.europa.eu/france/news/20210421/nouvelles_regles_europeennes_intelligence_artificielle_fr) ». Afin d’estimer les risques que pourraient représenter l’IA pour les citoyens et citoyennes, la CE propose un classement qui détermine le niveau de régulation nécessaire pour chaque domaine. La catégorie « haut risque » comprend par exemple les logiciels de recrutement ou les prises de décision automatisées dans l’attribution d’un crédit, situations où les biais sont souvent présents. La situation est encore différente en Chine, où le gouvernement a publié un plan dans le but de devenir le leader mondial dans le domaine de l'IA d'ici 2030. Pour atteindre cet objectif, l'Etat n'entend  pas réguler l'IA mais encourage et soutient les srtat-ups et entrerpises impliquées dans le domaine. 

Les perspectives de règlementation du numérique sont bien présentes en Europe, même s’il faudra vraisemblablement attendre encore quelques années avant l’entrée en vigueur de cet ensemble de lois. La course à l'IA entre les États-Unis et la Chine n'encourage pas une régulation contraignante des pratiques par le politique.


**La Singularité technologique** (encadré)

La Singularité technologique correspond au moment hypothétique du dépassement de l’intelligence humaine par l’intelligence artificielle. Plusieurs scientifiques dont Ray Kurzweil, Stephen Hawking et Elon Musk ont fait part de leurs inquiétudes quant aux dangers potentiels d’une technologie qui deviendra tôt ou tard, supérieure aux humains.

La théorie de la singularité est basée sur la loi de Moore qui illustre l’évolution exponentielle de la puissance de calcul des ordinateurs. En effet, depuis les premiers microprocesseurs des années 1970, on observe que le nombre de transistors double environ tous les deux ans. Les défenseurs de la singularité partent du principe que cette croissance exponentielle continuera jusqu’à ce que les machines soient elles-mêmes capables de programmer d’autres machines. 

Or, ces prédictions omettent plusieurs facteurs et il parait aujourd’hui difficile de penser que la croissance technologique poursuive sa route vers l’infini.  Les limites matérielles et énergétiques ne sont par exemple pas prises en compte. Les détracteurs de la singularité considèrent que ces prédictions relèvent plus de la science-fiction que de faits scientifiques fiables. 

Pour aller plus loin: 
Jean-Gabriel Ganascia (2017), Le mythe de la Singularité. Faut-il craindre l’intelligence artificielle. Édition du Seuil.

<p id="footnote-1">[1] "Artificial Intelligence Index Report 2021", https://aiindex.stanford.edu/wp-content/uploads/2021/03/2021-AI-Index-Report-_Chapter-3.pdf, HAI Stanford University
 p. 14.
</p>

<p id="footnote-2">[2] "Le smartphone est au coeur de nos vies – Seuls 8% de la population suisse n'en possèdent pas encore", Deloitte
https://www2.deloitte.com/ch/fr/pages/press-releases/articles/deloitte-in-switzerland-smartphones-become-control-centre.html
</p>

<p id="footnote-3"> [3] Sara Ibrahim, "Des vaccins en un temps record grâce à l'intelligence artificielle" 
https://www.swissinfo.ch/fre/ai-e-vaccini_des-vaccins-en-un-temps-record--l-intelligence-artificielle-apporte-sa-contribution-%C3%A0-la-science/46260326
### Ressources 

* [Le sous-chapitre](https://www.boullier.bzh/livres/boullier-dominique-sociologie-du-numerique/) "Science-fiction et mythologie du numérique" du livre *Sociologie du numérique* (2016) de Dominique Boullier pour une discussion concernant les liens entre la science-fiction et le numérique. (303-306)

* [Le sous-chapitre](https://www.pressesdesciencespo.fr/fr/book/?gcoi=27246100540390) "L'intelligence artificielle" dans le livre Culture numérique de Dominique Cardon pour une brève présentation de l'IA. (385-398)

* [Le livre](https://www.seuil.com/ouvrage/le-mythe-de-la-singularite-jean-gabriel-ganascia/9782021309997) *Le mythe de la singularité* (2017) de Jean-Gabriel Ganascia 

* [Le documentaire](https://www.youtube.com/watch?v=WXuK6gekU1Y&t=3466s) AlphaGo - The Movie (2017) de Greg Kohs pour comprendre la victoire d'AlphaGo sur Lee Sedol

* [Un reportage](https://www.rts.ch/info/sciences-tech/technologies/11684864-lalgorithme-de-facebook-est-sexiste-pour-les-offres-demploi.html) de l'émission Mise au point de la RTS pour un exemple de biais engendré par un algorithme de Facebook. 

### Glossaire

* Système expert
* Apprentissage automatique ou *machine learning*
* Apprentissage profond ou *deep learning*
* Réseaux de neurones
* *Chatbot*


<br>

## Pistes pédagogiques 

<br>

<div align="left"; style="font-size:20px ;color:rgb(0, 0, 0); font-family:helvetica">
  <b>1. Le jeu de l'imitation 2021</b>
</div>

Objectif : Prendre conscience d
es forces et des faiblesses d'un assistant vocal de type Siri ou Alexa

Matériel: 
* Un assistant vocal 
* Une liste de [questions](https://www.aiunplugged.org/activity5-german.pdf) (En allemand pour l'instant)


Par groupe de 3 trois, les élèves posent tour à tour les questions de la liste à un assistant vocal. 
