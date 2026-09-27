---
title: Publier une photo
permalink: /fr/publier/
---

Cette page dit comment une photo passe de votre téléphone aux gens que vous
avez choisis, et ce qui lui arrive ensuite. La plupart du temps cela marche
comme vous vous y attendez. Là où ce n'est pas le cas, une décision est
généralement derrière&#160;: dans *people you know*, une publication est livrée
à des gens, pas publiée à un endroit. Il n'y a pas de page où elle se pose pour
que quelqu'un tombe dessus, pas d'adresse web pour elle, et aucun réglage qui
en créerait une. La publication publique n'existe pas ici.

**Dernière mise à jour&#160;:** 18 septembre 2026. Cette page décrit la bêta
fermée.

## Choisir les photos et les vidéos

La marque la plus à droite de la barre du bas ouvre l'écran de publication. Son
libellé est *publier*, qui est aussi le titre de l'écran qu'elle ouvre et le mot
du lien qui publie.

Les photos et les vidéos viennent du sélecteur d'Android lui-même. *people you
know* n'a aucune permission de lire votre photothèque et n'en demande
jamais&#160;: le sélecteur remet à l'application ce que vous avez choisi et
rien d'autre. L'application demande au téléphone l'accès à internet, les
notifications, et, sur Android 9 et antérieur seulement, la permission d'écrire
une photo enregistrée dans votre galerie. C'est toute la liste.

Une publication en contient jusqu'à 32, photos et vidéos ensemble dans
n'importe quel ordre. *choisir des photos et des vidéos* devient *en ajouter*
une fois que quelque chose est choisi, et le nombre à côté dit ce que vous
avez&#160;: *1 photo*, *4 photos*, *1 vidéo*, ou *3 photos et 1 vidéo*. Chaque
ligne est un petit carré de la photo elle-même avec *retirer* à côté et une
poignée *=* qui la fait glisser à une nouvelle place&#160;; l'ordre des lignes
est l'ordre des photos dans la publication. Choisir deux fois la même photo ne
l'ajoute qu'une fois. La limite n'est mentionnée que lorsque vous l'atteignez
vraiment, et elle le dit alors franchement&#160;: *C'est le maximum de photos
et de vidéos pour une publication (32).*

Il n'y a pas d'outil de recadrage, pas de filtre, pas de rotation et pas
d'annotation. Ce que vous choisissez est ce qui est publié, et rien de ce que
vous publiez n'est jamais recadré. La seule image recadrée du produit est votre
propre photo de profil, qui doit remplir un cercle à côté d'un nom. Le petit
carré à côté de chaque ligne ici, et les tuiles de la grille qui dessine une
longue publication, sont des planches-contact&#160;: des aperçus carrés d'une
photo qui est gardée entière.

### Toutes les données EXIF sont parties, parce qu'il ne reste rien à retirer

Chaque photo est décodée et réencodée sur votre téléphone avant d'être scellée.
Une image décodée n'a pas d'EXIF, donc chaque donnée est simplement absente de
ce qui quitte le téléphone&#160;: GPS, modèle d'appareil, numéros de série,
objectif, le logiciel qui a écrit le fichier. Rien n'est filtré, donc rien ne
peut échapper à un filtre.

La seule chose gardée est le moment où l'image a été prise, et elle voyage à
l'intérieur des données scellées plutôt que sur le fichier, parce que réécrire
une donnée sur un JPEG voudrait dire poser une photo déchiffrée sur le disque
le temps de l'écriture. Rien dans cette chaîne n'écrit de photo lisible
ailleurs que dans la mémoire. La seule exception délibérée est *enregistrer la
photo*, plus bas, qui est tout l'intérêt d'enregistrer.

## Publier une vidéo

La ligne d'une vidéo montre une image fixe de la vidéo avec une petite marque
qui dit qu'elle se lit, et pour le reste c'est une ligne comme les
autres&#160;: *retirer*, la poignée *=*, et sa place dans l'ordre.

### Une vidéo de plus d'une minute en garde une minute

Une vidéo peut durer environ une minute. Une plus longue n'est pas refusée. Sa
ligne porte *choisir quelle minute*, qui ouvre une image fixe de la vidéo avec
un curseur dessous. Déplacer le curseur déplace le début de la minute gardée,
et l'image suit, pour que vous trouviez le passage voulu en le regardant plutôt
qu'en lisant des temps. La poignée du curseur occupe la même part de la ligne
que la minute dans la vidéo entière&#160;: un tiers de la ligne pour une vidéo
de trois minutes, presque toute la ligne pour une vidéo de soixante-dix
secondes. Vous voyez ainsi combien vous gardez et où cela s'arrête. Il n'y a de
temps nulle part, et pas de seconde poignée, parce que la durée est toujours la
même minute&#160;; aller jusqu'au bout garde la dernière. Si vous ne choisissez
rien, la première minute est gardée.

### Ce qui arrive à une vidéo

Elle est convertie sur votre téléphone avant d'être scellée&#160;: dans le
format que tous les téléphones lisent, pas plus de 1080 pixels sur son petit
côté, et assez légère pour qu'une minute voyage sur la connexion d'un
téléphone. Comme une photo, elle ne garde du fichier d'origine que ses images
et son son. Le lieu, l'appareil et toutes les autres données sont partis, et le
moment où elle a été filmée voyage à l'intérieur des données scellées, comme
celui d'une photo. Ce que vous voyez sur la ligne est une image fixe de la
vidéo convertie, et c'est aussi ce que tout le monde voit avant de la toucher.

La conversion est le seul moment où cette application écrit en clair, sur le
stockage de votre téléphone, quelque chose que vous publiez. Un convertisseur
écrit un fichier, donc la copie convertie reste dans le cache de l'application,
que rien ne sauvegarde, le temps de la sceller, et elle est supprimée dès
qu'elle est scellée. C'est une copie plus petite d'une vidéo qui est déjà dans
votre photothèque. Tout ce qui quitte le téléphone est scellé sous la clé de la
publication, un morceau à la fois.

### Comment une vidéo se lit

Rien ne se lit tant que vous ne le demandez pas. Dans l'accueil, une vidéo est
une image fixe avec la marque par-dessus, et la toucher ouvre la publication et
la lit. Sur la publication et dans la visionneuse plein écran, un toucher la
lit, un second la met en pause, et à la fin elle revient à son image fixe. Elle
se lit avec son son, au volume de votre téléphone. Il n'y a pas de réglage du
son dans l'application, parce que rien ne s'y lit sans que vous l'ayez touché.
Passer à une autre photo l'arrête.

Une vidéo que vous recevez n'est jamais écrite sur votre téléphone, sauf si
vous l'enregistrez&#160;: elle se lit directement depuis sa copie scellée, un
morceau à la fois, et rien de lisible ne reste quand elle s'arrête.

## La légende

Le champ dit *dire quelque chose (facultatif)*, et il le pense. Une légende
peut aller jusqu'à quelques milliers de caractères et il n'y a pas de
compteur.

Elle est scellée dans la même enveloppe que le reste des données de la
publication&#160;: les dimensions de chaque image, son flou de remplacement, et
l'heure de prise de vue. Il n'y a pas de légende à envoyer toute seule.

Vous pouvez la modifier indéfiniment, depuis *options → modifier la légende*
sur votre propre publication, et vider le champ la supprime entièrement. Une
modification rouvre toute cette enveloppe scellée, remplace le seul champ et la
rescelle sous la même clé, donc ce que notre serveur voit est un nouveau bloc
qui arrive. Il ne peut pas dire que c'est la légende qui a changé. Une
publication modifiée porte le mot *modifiée* dessous, et la limite honnête
mérite d'être dite&#160;: un serveur malhonnête pourrait poser ce marqueur ou
le cacher. Il ne pourrait pas fabriquer une légende, ce qui demanderait la clé
de la publication.

## Choisir qui la voit

Le titre au-dessus du sélecteur est *qui voit ça*. Vos
[groupes](/how-it-works/groups/) viennent d'abord, puis une liste de vos
relations individuelles que l'on peut fouiller, en une seule liste de cases
plutôt qu'un changement de mode. Une publication peut être adressée à plusieurs
groupes à la fois, ou à un groupe plus une personne, ou à une personne.

Seules vos relations peuvent être parmi les destinataires que vous
choisissez&#160;: des gens avec qui vous et eux avez accepté d'être en
relation. Il n'y a pas d'abonnés ici et rien d'adressé à l'ami d'un ami. La
seule exception est un album, plus bas, où les destinataires sont les membres
de l'album et peuvent comprendre des co-membres avec qui vous n'êtes pas en
relation.

Une publication adressée à exactement une personne est une publication, pas un
message. Elle a les mêmes commentaires et les mêmes réactions que n'importe
quelle autre, et il n'y a ni fil de discussion, ni indicateur de saisie, ni
boîte de réception nulle part dans l'application.

### Tout le monde est la seule case qui ne se combine avec rien

C'est la règle que la plupart des gens rencontrent en premier et trouvent
étrange. Cochez un groupe ou une personne et Tout le monde se vide&#160;: sa
case devient pâle et ne répond plus au toucher. Sa ligne ne change pas pour
autant, c'est le nombre de vos relations, parce que chaque ligne de cette liste
répond par un nombre.

La raison est arithmétique. Tout le monde se résout en toutes vos relations,
donc Famille est dedans et Ana est dedans. Cocher Famille à côté de Tout le
monde n'atteint personne de nouveau&#160;: les deux cases cochées livraient
exactement ce que Tout le monde seul livrait, et se lisaient à l'écran comme
quelque chose de plus petit que ce qui allait partir. Ce que cet écran prétend,
c'est que les destinataires sont choisis, et une sélection qui ne dit pas ce
qu'elle fait n'est pas un choix que quelqu'un a fait.

L'autre solution évidente a été refusée aussi. Une touche sur Tout le monde ne
balaie pas les autres cases, parce que des choses qui disparaissent sous votre
pouce sont un mauvais comportement partout et le pire sur l'écran qui décide
qui voit une photo. Décochez ce que vous aviez coché et la case de Tout le
monde revient à la vie.

### Le sélecteur s'ouvre là où vous l'avez laissé, et cette mémoire reste sur votre téléphone

L'écran de publication s'ouvre avec les cases de la dernière fois déjà cochées,
parce que le cas courant est les mêmes gens que la dernière fois et qu'il ne
devrait pas coûter autant de touches que le cas rare.

Ce souvenir est un petit fichier dans le stockage de l'application, gardé par
compte, et il ne nous est jamais envoyé. Les destinataires de votre dernière
publication sont un fait sur vos habitudes&#160;; notre serveur apprend déjà
les destinataires de chaque publication en la livrant, et il n'y a aucune
raison de lui remettre en plus une réponse permanente à la question de savoir à
qui cette personne parle d'habitude, interrogeable sans qu'aucune publication
soit faite. Le coût honnête est qu'un téléphone neuf ouvre un sélecteur non
coché.

Deux règles plus petites vont avec. L'ensemble mémorisé est réduit à ce que le
sélecteur dessine vraiment, donc un groupe que vous avez supprimé depuis ou
quelqu'un avec qui vous n'êtes plus en relation en sort en silence&#160;: une
case cochée que vous ne pouvez pas voir à l'écran n'est pas un choix que vous
avez fait. Et il n'est écrit qu'après qu'une publication a réellement abouti,
jamais depuis un brouillon qui a échoué.

### Contribuer à un album n'a pas de sélecteur du tout

*ajouter des photos* sur l'écran d'un album ouvre le même écran de publication
avec une ligne là où serait le sélecteur&#160;: *tout le monde dans Maine*. Les
membres sont les destinataires, et rien d'autre ne peut être nommé à côté.
Élargir veut dire ajouter quelqu'un à l'album, ce que couvre la [page des
albums](/how-it-works/albums/).

## Identifier quelqu'un sur une photo

Un lien *identifier* se trouve sur la ligne de chaque relation dans le
sélecteur, et seulement sur les lignes des relations qui ont laissé *autoriser
mes relations à m'identifier* activé, ce qu'il est jusqu'à ce qu'elles le
désactivent. Jusqu'à 32 personnes peuvent être identifiées sur une
publication.

Identifier quelqu'un coche sa case de destinataire et l'y maintient. Une
identification est un nom sur une photo que la personne peut voir, donc les
deux ne peuvent pas se séparer&#160;; *retirer l'identification* est la seule
façon de libérer la case, et elle ne la rend que si c'est l'identification qui
l'avait cochée.

Les noms apparaissent sous le nom de l'auteur comme *avec anna, bruno*, et
toute personne qui voit la publication les voit, pas seulement ceux qui les
connaissent. Un nom qui appartient à quelqu'un avec qui celui qui regarde n'a
aucune relation ouvre la fiche de cette personne. C'est l'un des rares endroits
ici où un inconnu vous est nommé&#160;: la liste des membres d'un album en est
un autre, et la liste de qui a choisi une réaction aussi, parce que les deux
sont les gens de quelqu'un d'autre plutôt que les vôtres.

Retirer un nom appartient à la personne nommée, depuis *options → retirer mon
identification*. En tant qu'auteur vous ne pouvez ni ajouter ni retirer un nom
après avoir publié.

Une fois quelqu'un identifié, une case apparaît&#160;: *les personnes
identifiées peuvent repartager*, désactivée par défaut et montrée seulement
quand il y a quelqu'un qu'elle pourrait concerner. Elle permet à toute personne
que vous avez nommée de transmettre la photo à ses propres relations, comme une
publication à elle dessinée sous votre nom et votre visage. Vous pouvez donner
cette permission ou la reprendre ensuite depuis la publication elle-même, et la
reprendre détruit les partages qui reposaient dessus.

Une personne que vous nommez l'apprend dans son onglet activité, et être nommé
est la seule chose pour laquelle l'interrupteur d'identification autorise son
téléphone à être notifié. La notification arrive à la place de celle qu'elle
aurait eue pour votre publication plutôt qu'à côté&#160;: une photo, une
interruption. Désactiver *autoriser mes relations à m'identifier* arrête
l'identification et la notification ensemble.

## Publier

Le lien *publier* en bas n'est pas touchable tant qu'il n'y a pas au moins une
photo et des destinataires. Il n'y a pas de message d'erreur pour n'avoir
choisi personne&#160;: le lien ne répond simplement pas.

Ensuite, sur votre téléphone, dans cet ordre&#160;: la clé de chaque
destinataire est récupérée et comparée à la copie que votre téléphone a épinglée
la première fois qu'il l'a vue&#160;; une clé neuve est faite pour cette
publication et pour aucune autre&#160;; chaque photo est décodée, réencodée,
scellée et relâchée, une à la fois, pour que trente-deux n'aient pas à tenir
ensemble en mémoire&#160;; les fichiers scellés sont envoyés&#160;; et la clé de
la publication est enveloppée une fois pour chaque destinataire et une fois
pour vous. Pendant ce temps le lien lit *publication en cours* à côté d'un
anneau qui se remplit. Il n'y a pas de pourcentage&#160;: un nombre invite au
calcul, et ce que vous voulez savoir est si c'est bientôt fini.

Si la clé d'un destinataire a changé depuis la dernière fois que votre
téléphone l'a vue, toute la publication s'arrête avant qu'un seul octet soit
envoyé et une alarme vous est montrée, nommant cette personne. Envoyer à tout
le monde sauf elle serait le pire des deux résultats&#160;: la photo part quand
même, et le seul signal que quelque chose ne va pas devient quelque chose que
l'on dépasse en continuant.

La publication et chaque livraison sont écrites ensemble ou pas du tout, et les
destinataires sont résolus à nouveau à cet instant. Quelqu'un que vous avez
retiré un instant plus tôt en sort, et notre serveur ne livre à personne en
dehors des destinataires que votre téléphone a déclarés, même si un téléphone
essayait. C'est notre serveur qui vérifie un téléphone&#160;; ce qu'un téléphone
peut vérifier de notre serveur est plus étroit, et [comment marche la
confidentialité](/fr/confidentialite/) dit où cela s'arrête.

### Où vous atterrissez

L'écran de publication se ferme et vous êtes sur votre propre profil, où la
publication que vous venez de faire est la ligne la plus récente – sauf si
c'était une contribution, qui atterrit sur l'album où elle est allée. Rien ne
dit «&#160;publié&#160;». L'annoncer serait le produit en train de se
féliciter.

Rien ne vous dit non plus combien de personnes l'ont reçue. Notre serveur
répond bien à votre téléphone avec un compte de destinataires, puisqu'il vient
de faire ce nombre de livraisons, et l'application ne le dessine nulle part.
Rien dans cette application ne compte jusqu'où une publication est allée.

### Votre propre publication n'est pas dans votre propre accueil

Il n'y a pas de livraison de vous vers vous. Votre copie de la clé de la
publication est une colonne sur la publication elle-même, ce qui est ce qui
vous laisse lire vos propres archives et partager la publication avec quelqu'un
plus tard. [Votre accueil](/fr/accueil/) est une file de ce que d'autres vous
ont envoyé&#160;; vos publications vivent sur votre profil.

### Quand une publication est refusée

- Adresser à Tout le monde avant d'avoir la moindre relation&#160;: il n'y a
  encore personne parmi ces destinataires.
- Beaucoup d'envois en une heure&#160;: *Cela fait beaucoup d'un coup.
  Réessayez plus tard.* Le refus n'énonce jamais le nombre, ni laquelle des
  limites c'était.

Une photo que le téléphone ne peut pas décoder fait échouer la publication avec
une phrase, et rien n'est envoyé. Une vidéo aussi&#160;: *Une vidéo de cette
publication n'a pas pu être lue. Essayez de la choisir à nouveau.* Une vidéo
dont la conversion sort trop lourde est convertie à nouveau, plus légère, et
c'est seulement quand deux essais de plus n'ont pas suffi que la publication
dit *Une vidéo de cette publication est trop lourde pour être partagée.
Essayez-en une plus courte.*

Deux autres refus vivent sur notre serveur et sont des filets plutôt que des
phrases que vous devriez jamais lire&#160;: plus de 32 photos, et un fichier
seul trop gros pour que nous le prenions. Le sélecteur s'arrête à 32 avant que
le premier puisse arriver, et le réencodage plus bas met chaque photo très
en-dessous du second.

## Comment une publication est dessinée

Jusqu'à huit photos forment un carrousel que vous faites défiler, avec des
points dessous. Neuf ou plus deviennent une grille de deux sur deux des quatre
premières dans l'ordre où vous les avez mises, avec un lien qui lit *voir les
24 ->* – le nombre propre à la publication – vers l'écran complet. Les quatre
premières, pas les quatre meilleures&#160;: choisir les quatre meilleures
serait cette application en train de classer les photos de quelqu'un, ce qui
est la seule chose qu'elle ne fait pas.

Aucune photo n'est jamais stockée ni envoyée recadrée, et aucune n'est refusée
pour sa forme. Ce qui est borné, c'est la boîte où elle est dessinée, et
seulement pour qu'une image ne puisse pas posséder l'écran&#160;: entre 1:2 et
2:1, et jamais plus haute que trois cinquièmes de l'écran. Une photo 4:3 prise
avec un téléphone tenu droit se situe exactement à cette seconde borne et est
dessinée sur toute la largeur de la ligne. Un recadrage 9:16, un panorama
assemblé ou une longue capture d'écran est logé entier dans la boîte, plus
petit, avec des marges, pour que rien ne soit caché. La toucher ouvre l'écran
complet, qui n'a aucune borne, et c'est ce que «&#160;voir la chose
entière&#160;» veut dire ici.

Ce qui est stocké n'est pas l'original de votre appareil. Chaque photo est
réencodée sur le téléphone à au plus 3 200 pixels sur son grand côté – un
plafond et jamais un agrandissement, donc une photo plus petite est laissée à
sa taille – ce qui suffit à ce qu'elle soit correcte sur un vrai écran
d'ordinateur et pas seulement sur un téléphone. C'est pourquoi le libellé de
l'application dit *enregistrer la photo* et pas «&#160;enregistrer
l'original&#160;»&#160;: il ne promettra pas une chose que nous ne gardons pas.

## Il n'y a pas de brouillons

Rien d'une publication que vous n'avez pas envoyée n'est écrit sur votre
téléphone. Les photos que vous avez choisies, la légende que vous avez tapée et
les cases que vous avez cochées vivent dans l'écran et partent avec lui.

Quitter demande donc, une fois, si vous avez choisi ou tapé quelque chose. Le
dialogue s'intitule *abandonner* et dit&#160;: *Rien ne sera publié, et ce que
vous avez choisi sera perdu.* La flèche en haut et le geste de retour du
système passent tous deux par cette même question, ce qui n'a pas toujours été
vrai&#160;: le geste passait juste à côté, et une garde qu'une des deux sorties
ignore n'est pas une garde.

### Une publication envoyée est écrite jusqu'à ce qu'elle parte

Dès que vous touchez *publier*, l'application vous a dit qu'elle l'envoyait, et
elle tient parole même si elle se ferme. Une publication en route – et elle
seule – est donc écrite sur votre téléphone&#160;: la légende, pour qui elle
est, et une copie de chaque photo et de chaque vidéo, dans l'espace propre à
l'application, qu'aucune sauvegarde ne copie et que rien d'autre sur le
téléphone ne peut lire. Tout est supprimé dès que la publication part, et dès
que vous l'abandonnez.

Si l'application se ferme avant qu'elle parte – vous l'avez balayée, elle a
planté, votre téléphone avait besoin de la mémoire pour autre chose – la
publication vous attend au prochain démarrage, en haut de votre profil, avec
cette phrase&#160;: *Cette publication n'est pas partie. Rien n'a été publié.*
En dessous se trouvent les deux mêmes choses que porte toute publication
arrêtée&#160;: *réessayer*, qui envoie cette même publication et non une
seconde copie, et *abandonner*, qui la jette et supprime les copies avec elle.
Rien n'est jamais renvoyé tout seul. Une publication composée mardi ne part pas
jeudi parce que vous avez ouvert l'application.

## Partager une publication à plus de gens ensuite

*options → partager à d'autres* sur votre propre publication rouvre le
sélecteur, avec une différence&#160;: tous ceux à qui la publication est déjà
allée sont cochés et ne peuvent pas être décochés, chaque ligne marquée *déjà
partagé*. Seul ce que vous cochez en plus est envoyé. L'action est *ajouter* et
la confirmation est le seul mot *ajouté*, sans nombre. Quand il ne reste
personne, l'écran dit *toutes vos relations l'ont déjà*.

Le cas d'usage est celui que tout le monde a. Les photos du bébé sont allées à
Tout le monde en mars. Ana est devenue une relation en août. En septembre vous
en ouvrez une et vous l'ajoutez, et elle la reçoit.

C'est l'une des deux façons dont les destinataires s'élargissent, et les deux
sont des choses que vous avez faites exprès. L'autre est *partager le
passé*&#160;: quand quelqu'un devient une relation, ou est ajouté à un groupe,
l'application propose de partager ce que vous aviez déjà publié pour Tout le
monde ou pour ce groupe, par nom et une personne à la fois. La [page des
relations](/how-it-works/people/) et la [page des
groupes](/how-it-works/groups/) le couvrent. Le travail sur les clés est le
même dans les deux cas, et il se passe sur votre téléphone&#160;: il ouvre
votre propre copie de la clé de la publication et l'enveloppe à nouveau pour
Ana. Notre serveur n'a jamais détenu de clé qu'il aurait pu lui remettre, ce
qui est aussi pourquoi Ana en faisant défiler votre profil ne peut rien lui
accorder en douce.

Deux conséquences des dates méritent d'être connues. Une publication ajoutée
aux destinataires de quelqu'un est datée de maintenant, donc elle arrive dans
son accueil comme une nouveauté plutôt que de couler là où mars la mettrait,
tandis que la ligne elle-même dit toujours *publié le 3 mars*. Et ajouter un
groupe prend les membres de ce groupe au moment où vous l'ajoutez, exactement
comme publier le fait.

*partager à d'autres* n'est pas proposé sur une contribution à un album, dont
les destinataires sont l'album, ni sur un partage, dont les destinataires sont
ce que la personne qui a repartagé a choisi une fois.

### Rien ne peut sortir quelqu'un d'une publication

Il n'y a de commande pour cela nulle part, et ce n'est pas un oubli. Quand la
publication a été faite, la clé a été enveloppée pour chaque destinataire du
moment, et elle est déjà sur son téléphone. Reprendre une permission n'aiderait
pas&#160;; ce qui marche, c'est détruire la clé.

Il y a donc deux remèdes, et tous deux sont plus grands que la publication.
[Retirer quelqu'un](/how-it-works/people/) de vos relations, ou le bloquer,
détruit les clés enveloppées entre vous dans les deux sens. *supprimer pour
tout le monde* reprend la publication à tout le monde d'un coup. Ce qu'aucun
des deux ne peut faire, c'est atteindre une photo que quelqu'un a déjà
téléchargée ou capturée, et aucune application ne le peut.

## Enregistrer une photo depuis une publication

Toute personne qui voit une publication peut en enregistrer les photos, depuis
*options → enregistrer la photo*. Cela enregistre celle que vous regardez, qui
n'est pas forcément celle à laquelle la publication s'est ouverte, et cela suit
votre défilement à l'instant où vous défilez&#160;: quelle photo suis-je en
train d'enregistrer n'est pas une question qui doit traîner derrière votre
pouce. Cela récupère toujours la copie pleine taille, même quand la plus petite
est déjà à l'écran.

Les fichiers atterrissent dans *Pictures/people you know/* sur Android 10 et
suivants, et dans la galerie sans ce dossier sur Android 9 et antérieur. Une
vidéo s'enregistre de la même façon, depuis *options → enregistrer la vidéo*,
dans *Movies/people you know/*&#160;: la minute qui a été publiée, telle
qu'elle a été convertie, et non le fichier dont elle a été faite. La
confirmation est un bandeau qui lit *enregistrée dans vos photos*. L'heure de
prise de vue est remise comme date du fichier, pour qu'une photo de 2019 se
range où elle doit dans votre galerie plutôt qu'en haut datée d'aujourd'hui.
Tout le reste de ce qui était sur le fichier d'origine a toujours disparu,
parce que c'était parti avant même que la photo quitte le téléphone qui l'a
prise.

Les captures d'écran ne sont pas bloquées. Ce que vous partagez avec quelqu'un,
il peut le garder, comme avec n'importe quelle autre façon d'envoyer une
photo.

## Supprimer une publication

*options → supprimer pour tout le monde*, sur votre propre publication. La
confirmation est une phrase plutôt qu'un «&#160;êtes-vous sûr&#160;»&#160;:
*Tout le monde perd cette photo immédiatement, et elle ne peut pas être
récupérée.*, suivie de la date à laquelle les fichiers quittent nos serveurs.

À la touche, chaque copie enveloppée de la clé de la publication est
détruite&#160;: celles des destinataires et la vôtre. Les commentaires étaient
scellés sous cette même clé, donc ils se ferment avec elle. Huit jours plus
tard, les fichiers chiffrés quittent le stockage, et les réactions partent avec
eux&#160;: une réaction est un seul émoji et n'a jamais été chiffrée. Ce qui
reste est la ligne de la publication, marquée supprimée, qui dit encore quand
elle a été faite et à qui elle était adressée&#160;; la [politique de
confidentialité](/privacy/) l'énumère.

Ces huit jours ne sont ni un délai de grâce ni un retour en arrière. Huit jours
après, le chiffré est exactement aussi illisible qu'au premier jour&#160;; il
n'y a rien qu'un retour en arrière pourrait restaurer. La confirmation nomme la
date plutôt que d'en faire le compte à rebours, ce qui est l'habitude dans
toute l'application.

Supprimer n'est jamais conditionné. Un compte suspendu peut toujours supprimer
ses propres publications, parce que c'est l'acte qui réduit plutôt que celui
qui ajoute, et ce qui reste publié ne doit pas dépendre de l'état d'un compte.

## Vos propres publications

La marque de la personne sur la barre ouvre votre propre profil, qui est aussi
là où publier vous amène. Sous votre visage, les gens que vous connaissez, vos
groupes et vos albums, il y a *vos publications*&#160;: une ligne par
publication, avec sa légende et la ligne *publié le 3 mars*. Avant que vous en
ayez fait la moindre, cela lit *rien pour l'instant*.

Il n'y a pas de compteur dessus et rien qui grandisse. Ce n'est visible que par
vous. Demander votre propre profil comme quelqu'un d'autre le ferait ne renvoie
rien, parce qu'un profil ici est simplement les publications de cette personne
pour lesquelles vous détenez personnellement une livraison, et vous n'en
détenez aucune de vous-même. Ce qu'une autre personne voit de vous est ce que
vous avez partagé avec elle, et cela diffère selon la personne, donc il n'y a
pas de version unique à prévisualiser.

## Ce qu'il n'y a aucun moyen de faire

Cela mérite d'être dit franchement, parce que plusieurs de ces choses sont
courantes ailleurs&#160;:

- Rendre une publication publique, donner à quelqu'un une adresse web pour
  elle, ou laisser quelqu'un en voir une sans y être destinataire ni la
  recevoir comme un partage que vous avez permis.
- Ajouter, remplacer ou réordonner des photos après avoir publié. Ce qui peut
  encore changer sur une publication faite, c'est la légende, les
  destinataires, et si les personnes identifiées peuvent la repartager.
- Sortir une personne des destinataires d'une publication.
- Programmer une publication, ou enregistrer un brouillon.
- Savoir qui a regardé une publication, ou combien de gens l'ont reçue.
  Personne n'apprend ici qui a regardé quoi que ce soit, y compris vous pour
  vos propres publications.
- Recadrer, filtrer, tourner ou retoucher une photo que vous publiez.
- Publier un texte seul ou un lien, ou une vidéo de plus d'une minute
  environ&#160;; une plus longue garde la minute que vous choisissez.
- Lire une vidéo sans la toucher, ou en baisser le son ailleurs que sur le
  téléphone lui-même.

Le [reste du guide](/fr/comment-ca-marche/) couvre les autres moitiés de
ceci&#160;: qui peut entendre un [commentaire](/how-it-works/comments/) sur une
publication, ce qu'un [groupe](/how-it-works/groups/) fait et ne fait pas, et
ce qui arrive à une photo quand quelqu'un est
[retiré](/how-it-works/people/). La [politique de
confidentialité](/privacy/) dit exactement ce que nous détenons pendant que
tout cela se produit.
