# COURS HTML

Ce recap de la seance est uniquement pour vous faire un rappel de ce que l'on a vu en cours cette semaine c'est en aucun cas un rappel exhausitf de toutes les notions vues en cours. Je vous encourage grandement a faire des recherches de votre coté sur n'importe quelle notion aborde ici. Je ne sais pas encore si je fairai ce genre de recap sur toutes nos seances, vous me donnerez vos avis la dessus j'y compte pas. 

# 1- Général

#### - Fonctionnement des sites WEB

Pour visiter un site WEB on se rend sur ce quon apelle un navigateur web. Le navigateur est un programme (process) qui tourne sur notre machine et qui a pour but principla de lire le code html et css pour afficher un résultat visuel a l'ecran.

##### Petite Histoire 😁

Le premier navigateur, originellement appelé WorldWideWeb (puis rebaptisé nexus) a été développé en 1990. Néanmoins le premier navigateur Web. En 1995 Internet Explorer 1 de Microsoft voit le jour.

Depuis 2000, Internet Explorer est le navigateur le plus utilisé, même si Mozilla Firefox progresse. Par ailleurs, il existe d’autres navigateurs dits "alternatifs" tels que Opera et Safari qui proposent des innovations et des solutions de qualité.

##### Principe et Fonctionnement

Le rôle d'un navigateur Web est principalement de permettre la consultation des informations disponibles sur le web. Lorsque l'on tape l'adresse d'un site (genre google.fr par exemple), le browser (un peu d'anglais fait pas de mal) se connecte au serveur WEB hébergeant le site et telecharge l'ensemble des ressources (fichier html, feuilles de styles, elements statiques ...). Et c'est tout ?? Don't Panic, On va voir exactement ce qui se passe juste apres ne vous affolez pas. Le protocole généralement utilisé est le protocole de communication HTTP.
Ensuite le moteur de rendu du navigateur traite la ressource et affiche le résultat sur l'écran de l'utilisateur
L’interface graphique sert à afficher le résultat et présente des boutons de navigation, une barre d'adresse et une barre d'état.

Les navigateurs sont capables de faire beaucoup de choses mais essayons de résumer les principales:
* lire le html lui indiquant le texte a afficher 
* interpreter le CSS (ou feuilles de style en cascade) permettant tout bonnement de styliser nos pages
* executer des scripts (notamment en JavaScript) 

De nombreux navigateurs existent aujoud'hui (Explorer ou Edge, Chrome, Safari, Firefox ..)

A vue de nez c'est tous les memes, cependant chaque navigateur affiche un meme site d'une maniere differente. 
Why ? Tout simplement parce que tous les browsers ne connaisent pas forecement les derniere fonctionnalites du HTML et du CSS.
Comme Explorer souvent en retard sur certaines fonctionnalités CSS.
Voila pourquoi les navigateurs se mettent a jour regulierement pour pouvoir beneficier notamment des dernieres fonctionnalités en vigeur.

Il faut egalement citer le fait que des navigateurs existent aussi pour les mobiles, ce sont generalament des version plus light des versions sur ordinateurs qui embarquent les memes fonctionnalites.


Ok cool on a vu ce que c'est un navigateur mais que se passe t'il exactement quand je visite un site web.

Je vous mets l'explication du site developer.mozilla.

> Lorsque vous saisissez une adresse web dans votre navigateur (dans notre comparaison, c'est comme aller au magasin) :

> 1.Le navigateur demande au DNS l'adresse réelle du serveur contenant le site web.
> 2.Le navigateur envoie une requête HTTP au serveur pour lui demander d'envoyer une copie du site web au client . Ce message, et les autres données envoyées entre le client et le serveur, sont échangés par l'intermédiaire de la connexion internet en utilisant TCP/IP.
> 3.Si le serveur accepte la requête émise par le client, le serveur envoie un message « 200 OK » au client qui signifie : « Pas de problème, tu peux consulter ce site web, le voici ». Ensuite le serveur commence à envoyer les fichiers du site web au navigateur sous forme d'une série de petits morceaux nommés "paquet" .
>4.le navigateur assemble les différents morceaux pour recomposer le site web en entier puis l'affiche sur votre écran .

DNS?? TCI/IP ?? HHTP ?? Késako 🤤

Un protocole est un ensemble de règles qui régissent les échanges de données entre des appareils connectés.
TCP/IP (Transmission Control Protocol / Internet Protocol) ce sont de protocoles definissent comment les doonees sont transmises sur le web.
HTTP (HyperText Transfer Protocol ) est un protocole d'application définissant le language de communication entre les clients et les serveurs.
Au niveau des protocoles je vous laisse faire vos recherches au niveau du modele TCI/IP ce n'est pas ici le sujet du cours.
Mainetant parlons un peu du DNS, c'est selon moi essentiel d'en parler.

Les vraies adresses Web ne sont pas les chaînes agréables et mémorisables que vous tapez dans votre barre d'adresse pour trouver vos sites Web favoris, mais des suites de chiffres. Ces suites de chiffre sont des nombres spéciaux qui ressemblent à ceci : 63.245.208.195.

Ce sont des adresses IP, elles reprseentent l'adresse d'une machine sur notre réseau. Mais vous vous imaginez taper une adresse IP sur votre navigateur ? Non et justement c'est la que le DNS rentre en jeu. Les serveurs DNS sont des serveurs spéciaux qui font correspondre une adresse web saisie dans le navigateur (par exemple google.com ) avec l'adresse réelle (IP) du serveur du site.

Si on le souhaite on peut tres bien taper l'adresse ip d'un serveur web pour y acceder.

Ok bon je pense qu'on a vu deja pas mal de choses jusqu'a maintenant et si on commencait a coder un peu ?

# 2-HTML

Jusque la on voit deja un peu plus clair sur le fonctionnement du WEB,parlons maintenant du HTML.

Un fichier html (HyperText Markup Language) c'est juste un fichier avec l'extension .html qui permet entre autres la mise en forme des pages et de leur contenu. Avec le html on peut comme son nom l'indique ecire de l'hypertexte mais pas que..
Développé en partie par le W3C (World Wide Web Consortium), le format ou langage HTML est apparu dans les années 1990. Il a progressivement subi des modifications et propose depuis 2014 une version HTML5 plus aboutie.

L'HTML est ce qui permet à un créateur de sites Web de gérer la manière dont le contenu de ses pages Web va s'afficher sur un écran, via le navigateur. Il repose sur un système de balises permettant de titrer, sous-titrer, mettre en gras, et plein d'autres choses, du texte et d'introduire des éléments interactifs comme des images, des liens, des vidéos... L'HTML est plus facilement compris des robots de crawl des moteurs de recherche que le language JavaScript, aussi utilisé pour rendre les pages plus interactives.
## Les balises
Comme dit un peu plus haut pour que le html soit compris par notre navigateur il faut utiliser des balises.
Elles se reperent facilement.
```
<titre>Ceci est un titre</titre>
```
Il existe plusieurs types de syntaxe de balises.

### Les balises en paires

```
<titre>Ceci est un titre</titre>
```
### Les balises orphelines

```
<image />
```

## Les attributs

Les attributs sont un peu les options des balises. Ils viennent les compléter pour donner des informations supplémentaires.

```
<image src="source de l'image"/>
```

Beaucoup d'attributs existent en html (src, alt, name, class, id ..), mais le but ici est de ne pas tout enumerer.

## Structure de base d'une page HTML5
```
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8" />
        <title>Titre</title>
    </head>

    <body>
    
    </body>
</html>
```

### Le Doctype

La toute première ligne s'appelle le doctype. Elle est indispensable car c'est elle qui indique qu'il s'agit bien d'une page web HTML.
Ce n'est pas vraiment une balise comme les autres (elle commence par un point d'exclamation). Vous pouvez considérer que c'est un peu l'exception qui confirme la règle.

### La balise html 
```
<html>

</html>
```

C'est la balise principale du code. Elle englobe tout le contenu de votre page. Comme vous pouvez le voir, la balise fermante </html>  se trouve tout à la fin du code !

### L'en-tête <head>  et le corps <body>

* L'en-tête <head>  : cette section donne quelques informations générales sur la page, comme son titre, l'encodage (pour la gestion des caractères spéciaux), etc. Cette section est généralement assez courte. Les informations que contient l'en-tête ne sont pas affichées sur la page, ce sont simplement des informations générales à destination de l'ordinateur. Elles sont cependant très importantes !

* Le corps <body>  : c'est là que se trouve la partie principale de la page. Tout ce que nous écrirons ici sera affiché à l'écran. C'est à l'intérieur du corps que nous écrirons la majeure partie de notre code.

#### L'encodage ( charset  )

L'encodage indique la façon dont le fichier est enregistré. C'est lui qui détermine comment les caractères spéciaux vont s'afficher (accents, idéogrammes chinois et japonais, caractères arabes, etc.).

Il y a plusieurs techniques d'encodage, portant des noms bizarres, et utilisées en fonction des langues : ISO-8859-1, OEM 775, Windows-1253…  UTF-8 est donc une méthode d'encodage comme les autres seulement c'est l'une des seules qui permet d'afficher sans aucun problème pratiquement tous les symboles de toutes les langues de notre planète ! C'est pour cela que j'ai indiqué utf-8  dans cette balise.

Je pense qu'au niveau du strict minimum pour commencer a taper sur notre IDE c'est bon !!






