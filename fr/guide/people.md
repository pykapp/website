---
title: Ajouter des relations
permalink: /fr/ajouter-des-relations/
---

Cette page explique comment deux personnes entrent en relation dans *people you
know*&#160;: comment on trouve quelqu'un, comment on demande, ce que la
personne apprend à chaque étape, et ce qui se passe quand on la retire ou qu'on
la bloque. Une bonne part n'est pas ce que font les autres applications, et là
où c'est le cas la raison est donnée plutôt que supposée.

## Il n'y a qu'une sorte de lien

Pas d'abonnements, pas d'abonnés, pas de liens à sens unique, pas de palier
«&#160;amis proches&#160;». Il y a un seul lien – une **relation** – et il
n'existe que parce que les deux personnes l'ont accepté&#160;: l'une demande,
l'autre accepte. Chaque côté peut y mettre fin à tout moment, seul, sans
l'accord de l'autre et sans le lui dire. L'écran d'inscription le dit en
quatre mots&#160;: *pas d'abonnés – que des relations réciproques*.

Tout le reste repose là-dessus. Quand vous publiez, votre téléphone chiffre la
photo avec une clé qui lui est propre et enveloppe une copie de cette clé pour
chaque personne à qui vous l'avez adressée. Être en relation est ce qui rend
une telle copie possible, et mettre fin au lien détruit les copies qui
existent. C'est pourquoi retirer quelqu'un ici reprend des photos plutôt que de
les cacher, et pourquoi rien de ce qui concerne le lien n'est rétroactif dans
un sens ou dans l'autre.

## Avoir un compte&#160;: les invitations

Pendant la bêta fermée nous délivrons les codes d'invitation à la main. Il n'y
a pas d'écran d'invitation dans l'application, rien à partager et aucun
quota&#160;: vous ne pouvez encore inviter personne. Garder la seule porte
d'entrée dans une seule paire de mains signifie un démarrage maîtrisé pour le
graphe, et aucun compte appartenant à des gens que personne ne connaît.

Un code fait douze caractères, tirés au hasard, sans les lettres et les
chiffres qui se ressemblent. Il est vérifié sur l'écran où vous le tapez plutôt
qu'à la fin de l'inscription, donc un code mal tapé est attrapé tout de suite.
Inconnu, expiré et déjà utilisé donnent tous une seule phrase – *Ce code
d'invitation ne peut pas être utilisé.* – parce que trois réponses différentes
diraient à quelqu'un qui devine laquelle de ses tentatives était proche. Les
codes expirent, et rien n'en réserve un pour vous entre le moment où vous le
vérifiez et celui où vous l'utilisez.

### Utiliser une invitation envoie une demande à qui vous a invité

C'est la partie à laquelle les gens ne s'attendent pas. Quand votre compte est
créé, votre téléphone envoie une demande d'ajout à la personne dont vous avez
utilisé le code, tout seul, au premier lancement. L'inscription le dit à
l'étape où le code est tapé&#160;: *La personne qui vous a invité recevra une
demande de votre part.*

Cela se produit sans aucune touche, donc c'est dit à l'avance&#160;;
l'apprendre après coup serait l'application agissant en votre nom sans le
mentionner.

Cela existe parce que sinon personne ne pourrait faire une première relation du
tout. Un compte neuf n'a aucune relation, donc il n'en partage aucune avec
personne, et la règle plus bas refuserait une demande dans les deux sens pour
toujours. L'invitation porte une permission durable de demander à cette
personne-là, et c'est tout ce qu'elle porte.

Elle achète exactement une présentation. La permission est dépensée par la
demande qu'elle autorise, donc si la personne refuse, ou si vous annulez, il ne
reste rien à envoyer et vous lui êtes un inconnu aux mêmes conditions que
n'importe qui. Cela marche dans un seul sens&#160;: vous pouvez lui demander.
Elle ne reçoit rien en retour, et n'a besoin de rien, parce que votre demande
est déjà en route vers elle.

De son côté, on le lui dit avant plutôt qu'après&#160;: le dialogue qui lui
demande de confirmer un refus dit *elle ne pourra plus vous demander* chaque
fois que c'est vrai, ce qui, pour un nouveau compte sans aucune relation, est
exactement le cas.

## Trouver quelqu'un

Par pseudo exact ou adresse de courriel exacte, et d'aucune autre façon. Le
libellé du champ est *pseudo ou e-mail*, la ligne dessous lit *La recherche
trouve les gens par leur pseudo ou leur e-mail exact.*, et au plus une personne
revient. Un pseudo partiel ne trouve personne. Une quasi-correspondance non
plus.

Il n'y a pas d'annuaire à parcourir, pas de suggestions, pas de «&#160;personnes
que vous connaissez peut-être&#160;», pas de liste d'amis d'amis, pas de
quasi-correspondances classées et aucune sorte de butinage. C'est le produit
plutôt qu'une fonctionnalité coupée faute de temps&#160;: une surface où des
inconnus peuvent être découverts est une surface où des inconnus s'accumulent,
et il n'est censé y avoir ici rien qui vaille d'être moissonné.

Une recherche qui ne trouve personne dit *personne de ce nom*, et elle dit
exactement cela pour un pseudo inconnu, pour votre propre pseudo, pour un
compte supprimé, et pour quelqu'un qui vous a bloqué ou que vous avez bloqué.
Aucun ne peut être distingué des autres, et l'exclusion est à l'intérieur de la
requête à la base plutôt qu'un filtre sur sa réponse&#160;: la ligne n'est
jamais lue du tout, donc il ne reste rien ensuite par quoi la réponse pourrait
différer.

La recherche est rationnée&#160;: 32 recherches par compte et par heure,
comptées sur une fenêtre glissante, facturées qu'elles trouvent quelqu'un ou
non. Personne n'ajoute trente-deux personnes en une heure, donc la limite est
généreuse pour une personne et inutile pour un recensement&#160;: 768 essais
par jour sont une erreur d'arrondi face à l'espace des pseudos possibles. Le
refus dit *Trop de recherches. Réessayez plus tard.* et ne récite jamais le
nombre. Vous renommer puise dans le même budget, parce que «&#160;ce pseudo
est-il pris&#160;» et «&#160;ce compte existe-t-il&#160;» sont la même
question.

Être trouvable est ce à quoi sert un pseudo, et il peut être changé depuis
*paramètres → votre pseudo*. L'ancien n'est pas gardé pour vous&#160;: les gens
qui le connaissaient ne vous trouveront plus ensuite, et quelqu'un d'autre peut
le prendre.

Un code de connexion va à une adresse de courriel et nulle part
ailleurs&#160;: l'application n'envoie pas de messages texte. La recherche ne
prend pas de numéro non plus, et pour la même raison. Un compte ne peut en
venir à détenir un numéro qu'en y recevant un code, donc le champ offrirait une
clé qui ne peut jamais correspondre, et facturerait un essai de recherche pour
rien.

Un compte peut aussi ne détenir **aucune adresse**, et s'ouvrir avec un mot de
passe à la place. Quelqu'un qui s'est inscrit ainsi se trouve par son pseudo et
par rien d'autre, ce qui est le compromis qu'il a choisi&#160;: nous ne détenons
aucune adresse pour lui.

## Demander à ajouter quelqu'un

Touchez *ajouter*. Votre téléphone enveloppe votre clé de profil pour la
personne à qui vous avez demandé, ce qui est ce qui permet à son téléphone
d'ouvrir votre nom affiché et votre photo&#160;; nous ne détenons que du
chiffré d'un bout à l'autre et ne pouvons lire ni l'un ni l'autre. La demande
expire après seize jours, et les deux côtés voient la date plutôt qu'un compte
à rebours.

De son côté, elle arrive en haut de son propre profil sous *vous ont demandé*,
au-dessus de qui elle connaît et au-dessus de ce qu'elle a fait, avec un point
sur la marque du profil dans la barre tant que quelqu'un attend. Le point n'est
jamais un nombre, et le regarder ne l'éteint pas – il s'éteint quand la
dernière demande est acceptée, refusée ou expirée. Il n'est délibérément pas
aussi sur l'écran des personnes, et une demande qui arrive n'écrit rien dans
l'onglet activité&#160;: une chose, à un seul endroit.

Une demande envoie aussi une notification. C'est l'une des deux seules que
l'application envoie sans qu'on le lui demande&#160;: l'autre est quelqu'un qui
met votre nom sur une photo, que vous pouvez arrêter à *paramètres → autoriser
mes relations à m'identifier*. Vous pouvez désactiver celle-ci à *paramètres →
notifications → quand quelqu'un veut m'ajouter*. Tout le reste de ce qui vous
interrompt est une chose que vous avez demandée. Les mots sont écrits par le
téléphone qui reçoit, à partir d'un nom que seul ce téléphone peut lire&#160;;
ce que nous envoyons est un simple jeton disant quel genre de chose s'est
produit.

Sa ligne montre votre visage et votre nom, avec *expire le 17 septembre* sous
le nom&#160;; puis *vous connaissez tous les deux anna, carla*&#160;; puis
*accepter*, *refuser* et *options* – qui contient *bloquer* et *signaler*,
parce que la demande d'un inconnu est le seul endroit d'où un abus peut arriver
de quelqu'un qui n'est sur aucun autre écran, et que refuser seulement lui
laisse la possibilité de redemander quand la règle plus bas le permet encore.
Votre nom a toute la largeur de la ligne, et toucher votre visage ou votre nom
ouvre votre fiche&#160;: le nom en entier, votre pseudo, ce que vous avez écrit
sur vous, et *accepter*.

*accepter* se fait en un geste, et *refuser* demande d'abord. Ce n'est pas une
question de gravité – c'est la seule règle derrière toutes les confirmations de
l'application&#160;: on demande quand toucher une deuxième fois ne défait rien.
Accepter a un retour en arrière, qui est *retirer* sur le profil ainsi créé.
Refuser n'en a aucun&#160;: la demande est réglée et la clé qui vous laissait
voir son visage est détruite dans le même mouvement. (*bloquer* demande aussi,
et *signaler* est une zone où l'on écrit plutôt qu'une question à franchir.)

### Ce que vous voyez pendant que vous attendez est presque rien

Votre propre demande sortante se trouve sur l'écran des personnes sous *vous
avez demandé*, et elle montre son pseudo, *annuler*, et la date. Pas de visage.
Pas de nom affiché. Pas de «&#160;vu&#160;». La ligne n'a aucun champ qui
pourrait dire si la personne l'a ouverte, et un tel champ n'existe nulle part.

L'asymétrie est toute la règle. La personne qui demande offre un visage et un
nom pour pouvoir être reconnue&#160;; la personne à qui on demande ne révèle
absolument rien jusqu'à ce qu'elle dise oui. C'est aussi pourquoi votre propre
ligne *vous connaissez tous les deux* est vide pour quelqu'un à qui vous avez
demandé et qui n'a pas répondu&#160;: lesquelles de vos connaissances la
connaissent est un fait sur ses relations, pas sur les vôtres.

### Accepter ne remet aucun historique

Accepter crée le lien et ne déplace aucune photo. Son profil commence vide –
*rien de partagé avec vous pour l'instant* – et ne se remplit qu'à mesure
qu'elle partage avec vous, et le vôtre fait de même. Il n'y a pas de catalogue
à ouvrir, parce qu'un profil ici n'est pas une page que quelqu'un
entretient&#160;: ce sont simplement ses publications qui vous ont été
envoyées.

Partager ce que vous aviez publié avant de vous rencontrer est une proposition
distincte à laquelle vous répondez exprès, sauf si vous avez activé *paramètres
→ partager les anciennes publications avec les nouvelles relations*, qui est
désactivé au départ et saute la question. Dans les deux cas, ce qui est partagé
atterrit sur votre profil plutôt que dans son accueil. La [page pour
publier](/fr/publier/) le couvre.

### Refuser, annuler, expirer

Les trois sont silencieux. Refuser détruit la clé de profil enveloppée dans la
transaction même qui règle la demande, et la personne qui a demandé n'apprend
rien&#160;: sa ligne sortante n'est simplement plus là. Annuler retire la ligne
du profil de l'autre personne sans aucune notification. L'expiration est
balayée plutôt que seulement filtrée, pour qu'une demande que personne n'a
jamais ouverte ne laisse pas votre profil déchiffrable par elle pour toujours.

Refuser demande d'abord, et le dialogue dit qui et quoi&#160;: *refuser
Delphine Marchand*, puis *Cette personne n'en sera pas informée. Sa demande
disparaît, et elle pourra vous redemander.* Quand elle ne le pourra pas –
personne en commun, et *demandes de tout le monde* désactivé – la deuxième
phrase le dit à la place, parce que c'est la version de ce geste qu'attendre
ne rattrape pas.

Une limite honnête, puisqu'il est facile de la lire comme plus forte qu'elle
n'est&#160;: ce qui est détruit, c'est la copie de votre clé de profil qui était
enveloppée pour cette personne, et la clé elle-même ne change pas. Nous cessons
de lui servir votre nom et votre photo, et cela ne fait pas oublier ce qui a
déjà été montré. [Comment marche la confidentialité](/fr/confidentialite/) dit
ce que cela laisse ouvert.

Si vous vous demandez l'un l'autre en même temps, les deux demandes restent là
et la première acceptation crée le lien et efface les deux.

## Qui peut vous demander

Par défaut, seulement les gens qui partagent une relation avec vous. C'est
activé pour chaque compte, et c'est la seule règle du produit contre laquelle
un inconnu bute.

C'est dit à l'inscription, sous le champ du pseudo, parce qu'un pseudo est ce
qui vous rend trouvable et que ceci est la réponse à la question que cela
soulève&#160;: *Seules les personnes ayant une relation en commun avec vous
peuvent demander à vous ajouter. Vous pouvez changer cela dans les
paramètres.* C'est montré et non choisi&#160;: une décision de plus à
l'inscription, à propos d'un réglage par défaut sur lequel personne ne peut
encore avoir d'avis, serait une chose de plus entre quelqu'un et
l'application.

L'interrupteur est *paramètres → demandes de tout le monde*. Il est désactivé,
et sa ligne lit *seulement les personnes ayant une relation en commun*&#160;;
activé, elle lit *tout le monde peut vous demander*. L'activer ne fait jamais
que vous rendre plus facile à joindre, et le désactiver ne fait jamais que vous
rendre plus difficile à joindre, donc rien d'autre dans l'application ne peut
le figer dans un sens ou dans l'autre.

Quelqu'un sans relation en commun se le fait dire franchement&#160;: *Il faut
une relation en commun pour envoyer une demande.* C'est le seul refus de
l'application qui s'explique. Partout ailleurs un refus est un ordinaire
«&#160;introuvable&#160;», parce que dire «&#160;vous n'avez pas le
droit&#160;» confirme que la chose existe. Ici cela ne confirme rien&#160;:
cette personne connaissait déjà votre pseudo, donc un «&#160;introuvable&#160;»
inventé serait un mensonge qui n'aiderait personne.

Les deux exceptions à la règle sont l'interrupteur de la personne visée et
l'invitation ci-dessus. Il n'y en a pas de troisième.

## Qui vous connaissez tous les deux

Là où l'application peut le montrer – sous une demande reçue, en haut du profil
d'une relation, sur une fiche de personne – cela lit *vous connaissez tous les
deux anna, carla*, et chaque nom ouvre le profil de cette personne.

Ce sont des noms et jamais un compte. «&#160;3 relations en commun&#160;» est
un chiffre que d'autres font grandir, ce que ce produit refuse partout, et
*lesquelles* trois est tout ce qui décide quoi que ce soit. Chaque nom de la
ligne est déjà une de vos propres relations – le recouvrement entre deux
ensembles de gens est à l'intérieur des deux – donc la ligne ne vous apprend
rien sur personne que vous ne connaissiez déjà.

Elle est vide dans un cas, exprès&#160;: une fiche pour quelqu'un à qui vous
avez demandé et qui n'a pas répondu.

## Quelqu'un qu'une connaissance a identifié sur une photo

Il y a deux façons d'arriver à une personne que vous n'avez jamais rencontrée,
et aucune n'est une recherche. Si une de vos relations identifie quelqu'un sur
une photo qu'elle vous a montrée, ce nom se touche&#160;; et si une relation
transmet la photo de quelqu'un d'autre, la ligne porte le nom de qui l'a faite
à l'origine. Les deux ouvrent la même fiche&#160;: son visage, son nom avec son
pseudo dessous, *vous connaissez tous les deux…*, et *ajouter*.

Deux accords tiennent derrière un nom sur une photo. Celui de la personne
elle-même, dans un réglage activé jusqu'à ce qu'elle le désactive, et celui de
l'auteur, dans le fait de la nommer. Une photo transmise a la même forme&#160;:
l'auteur d'origine a dû activer *les personnes identifiées peuvent repartager*,
qui est désactivé au départ, et l'une des personnes qu'il a nommées a dû
choisir de la transmettre. C'est le mécanisme qui existe déjà hors ligne –
«&#160;qui est-ce sur ta photo&#160;&#160;?&#160;» – et c'est le contraire de
«&#160;personnes que vous connaissez peut-être&#160;»&#160;: rien n'est
calculé, classé ni suggéré, et la personne au milieu répond de la
présentation.

La fiche répond pour une relation, pour quelqu'un avec qui une demande est en
cours dans un sens ou dans l'autre, pour quelqu'un identifié sur une photo que
vous détenez encore, et pour qui a fait à l'origine une photo qui vous a été
transmise. Pour toute autre personne c'est le même «&#160;introuvable&#160;»
qu'un compte qui n'a jamais existé, octet pour octet. Et ce qu'elle vous montre
dépend de ce qu'on vous a donné&#160;: pour quelqu'un qui vous a demandé elle
montre un visage, pour une relation elle montre un visage, et pour quelqu'un à
qui *vous* avez demandé elle montre un pseudo, les mots *demande envoyée*, et
rien d'autre.

## La limite est 128

Vous pouvez avoir 128 relations. C'est une limite dure&#160;: il n'y a pas de
recours, rien à acheter qui la relève, et rien à nous demander. Quand vous
l'atteignez, le refus nomme le nombre, parce que c'est votre propre compte –
*Vous avez déjà 128 relations. Retirez quelqu'un pour en ajouter une
nouvelle.* – et retirer quelqu'un est le seul remède.

Le nombre est ce qu'il est parce qu'on peut relever un plafond et qu'on ne peut
pas l'abaisser&#160;: l'abaisser laisse tous ceux au-dessus de la nouvelle
limite sans bonne réponse, donc l'asymétrie plaide pour commencer serré. Il se
situe aussi juste sous le nombre de Dunbar d'environ 150, qui est la thèse que
ce produit défend réellement.

Votre propre compte est sur votre propre profil, sous *vos relations*, qui lit
*relations 12 sur 128*, et le compte est lui-même le chemin vers l'écran des
personnes. C'est le seul nombre de son espèce dans l'application, et il survit
à la règle contre les totaux parce qu'il n'est aucune des choses qui rendent un
total corrosif&#160;: il est borné, il n'est visible que par vous, et il répond
à une question que vous vous posez vraiment – suis-je près de la limite – que
vous découvririez sinon en étant refusé au milieu d'un ajout.

Votre compte n'est jamais consulté quand quelqu'un vous envoie une demande.
Dire à un inconnu «&#160;cette personne est pleine&#160;» remettrait un fait
sur les relations de quelqu'un d'autre. La demande est faite, et la limite est
appliquée à l'acceptation, là où la personne qui l'apprend est celle dont c'est
le compte. Si c'est elle qui est pleine, celle qui accepte se le fait
dire&#160;: *Cette personne ne peut pas avoir plus de relations.*

## Ce que l'autre personne apprend, étape par étape

- **Vous la cherchez.** Rien, jamais. Chercher est invisible pour la personne
  cherchée.
- **Vous envoyez une demande.** Une notification sauf si elle l'a désactivée,
  une ligne sous *vous ont demandé* sur son propre profil, et un point sur sa
  marque de profil. Aucune entrée d'activité.
- **Elle l'ouvre.** Vous n'apprenez jamais qu'elle a regardé.
- **Elle refuse.** Vous n'apprenez rien&#160;; votre ligne sortante a
  simplement disparu.
- **Cela expire.** Rien. Vous aviez la date sur la ligne.
- **Vous annulez.** Rien.
- **Elle accepte.** Vous recevez une ligne d'activité&#160;: *anna a accepté
  votre demande*.
- **Vous la retirez.** Rien. Les deux côtés cessent discrètement de pouvoir
  ouvrir ce que l'autre a partagé.
- **Vous la bloquez.** Rien. Chaque porte répond exactement ce qu'elle
  répondrait pour un compte qui n'a jamais existé.
- **Vous la signalez.** Rien. Aucune route ne dit à une personne signalée
  qu'un signalement existe ni qui l'a déposé.
- **Vous êtes à 128.** Vous seul l'apprenez, et le nombre est nommé.
- **Elle est à 128.** Vous ne l'apprenez jamais en demandant. Seule la personne
  qui accepte l'apprend, à propos de son propre compte.

## Masquer quelqu'un

Un interrupteur sur son profil, sous *me prévenir quand elle publie*&#160;:
**masquer anna**. Il fait une seule chose – ses publications cessent d'arriver
dans votre accueil – et c'est la seule chose que vous puissiez faire à un lien,
dans cette application, qui ne détruit rien.

*Cette personne n'en sera pas informée. Ses publications restent sur ce profil
et quittent votre accueil.* Cette phrase est sous l'interrupteur parce que ce
sont les deux choses que l'étiquette ne peut pas dire, et ce sont les deux qui
comptent&#160;: masquer est silencieux, comme retirer et bloquer, et
contrairement à l'un et à l'autre cela n'enlève rien.

Ce que cela change, exactement&#160;:

- ses publications ne sont plus dans votre accueil, ni dans le compte de vos
  onglets&#160;;
- la notification *me prévenir quand elle publie*, si vous l'aviez activée,
  s'éteint – l'interrupteur juste au-dessus, sous vos yeux, au moment du
  geste&#160;;
- c'est tout.

Ce que cela laisse intact, c'est le reste, et cette liste-ci est plus longue que
la précédente à dessein&#160;:

- chaque photo qu'elle vous a envoyée reste à vous d'ouvrir, depuis son profil,
  là où elle a toujours été – rien n'est révoqué, aucune clé n'est
  détruite&#160;;
- *publications déjà vues* garde ce que vous avez regardé&#160;: masquer n'est
  pas dé-voir&#160;;
- un album que vous partagez ne change pas. Son écran montre ses contributions
  et sa propre pastille les compte, parce qu'un album est une pièce où vous avez
  choisi d'être et que son compte doit s'accorder avec ce qu'il s'apprête à vous
  montrer. Seul votre accueil est plus calme&#160;;
- commentaires, réactions, groupes, le lien lui-même&#160;: intacts.

Désactiver l'interrupteur remet la file en place, y compris ce qui est arrivé
pendant. La notification, elle, reste éteinte&#160;: c'est une préférence, et
elle est à un geste.

**Une photo que quelqu'un d'autre a repartagée arrive quand même.** Si carla est
masquée et que bruno repartage une de ses photos, vous la voyez&#160;: c'est
bruno qui a choisi de vous la mettre sous les yeux, et la ligne est la sienne.
Masquer bruno la fait disparaître.

**Personne n'est informé, et rien ne peut l'informer.** Aucune route ne comporte
de champ qui le rapporte, dans un sens ou dans l'autre. De son côté, masquée et
non masquée sont le même compte. Sa ligne sur l'écran des personnes indique
*publications masquées* sous l'identifiant, pour vous et pour personne
d'autre&#160;: tout l'effet d'un masquage est que quelque chose cesse
d'apparaître, il lui faut donc un endroit qui le dise.

**Masquer n'est pas bloquer en plus léger.** Bloquer concerne la sécurité et
fait beaucoup&#160;: cela retire, détruit les clés dans les deux sens, sort vos
mots des pièces de l'autre et refuse toute demande future. Masquer concerne
votre propre accueil un mardi. Si quelqu'un se comporte mal avec vous,
bloquez-le.

## Retirer quelqu'un

Depuis *options* sur son profil, à côté de *bloquer* et *signaler*. C'est la
seule porte, et l'écran des personnes n'en a aucune&#160;: chaque ligne y mène
à la personne, et ce que vous pouvez faire à son sujet est sur l'écran qui lui
est consacré. Un dialogue, titré du verbe et de son nom – *retirer Delphine
Marchand* – et il dit ce qui va se passer plutôt que de demander si vous êtes
sûr&#160;: *Cette personne n'en sera pas informée. Vous cesserez tous les deux
de voir ce que l'autre a partagé.*

Tous les dialogues de l'application qui décident au sujet d'une personne sont
titrés ainsi. C'est la dernière chose entre un pouce et quelque chose que rien
ne rend, et un menu *options* peut s'ouvrir sur la mauvaise ligne.

En une transaction, cela détruit le lien et, avec lui&#160;:

- chaque clé enveloppée qui laissait l'un ou l'autre ouvrir les publications de
  l'autre, dans les deux sens – donc les photos cessent d'être lisibles plutôt
  que d'être cachées&#160;;
- les deux autorisations de profil, donc aucun des deux ne se voit plus servir
  le nom affiché ni la photo de l'autre au titre de la relation. Une copie de
  votre clé de profil portée par la photo d'une tierce personne qui vous
  identifie, ou par un repartage d'une des vôtres, survit à un retrait, comme
  le dit [Comment marche la confidentialité](/fr/confidentialite/)&#160;;
- son appartenance à vos groupes, et la vôtre aux siens&#160;;
- son appartenance à tout [album](/how-it-works/albums/) que vous avez créé, et
  ses copies des clés de tout ce qu'il contient – et les vôtres de tout album
  qu'elle a créé&#160;;
- les abonnements «&#160;me prévenir quand cette personne publie&#160;», dans
  les deux sens&#160;;
- tout partage que l'un ou l'autre a fait des publications de l'autre.

Deux choses que cela ne fait pas. Cela n'atteint pas un album fait par une
tierce personne&#160;: si vous êtes tous les deux dans l'album de Carla, vous
continuez d'y recevoir vos contributions mutuelles, parce qu'une livraison
d'album repose sur le fait d'être dans la pièce plutôt que sur le lien entre
vous. Et cela ne peut pas dé-télécharger&#160;: tout ce qui est déjà sur son
téléphone lui appartient, exactement comme pour toute photo que vous avez
envoyée à quelqu'un par quelque moyen que ce soit. Ce qui s'arrête, c'est tout
ce qui est nouveau.

Un retrait se défait en se rajoutant l'un l'autre, et la proposition de
partager le passé peut rendre ce que la personne détenait. C'est la différence
entre cela et un blocage.

## Bloquer quelqu'un

Accessible sous *options* sur son profil, à côté de *retirer* et de
*signaler*&#160;; et sous *options* sur une demande reçue – parce qu'un simple refus laisse la
possibilité de redemander. Un inconnu peut être bloqué, et rien ne s'oppose
jamais à ce que vous bloquiez quelqu'un.

Le dialogue, titré *bloquer Delphine Marchand*&#160;: *Cette personne n'en sera
pas informée. Cela la retire aussi de vos relations, et elle ne pourra plus
vous demander.*

Tout ce que fait un retrait, et ensuite&#160;:

- **Chaque livraison entre vous s'en va, photos d'album comprises.** C'est le
  seul acte qui atteint une pièce faite par quelqu'un d'autre&#160;: ses photos
  cessent d'arriver par l'album de Carla, et plus rien de l'un ni de l'autre
  n'est jamais enveloppé pour l'autre.
- **Votre visage disparaît des photos des autres, pour l'un comme pour
  l'autre.** Quand une relation [vous nomme sur une photo](/fr/publier/), son
  téléphone enveloppe une copie de votre clé de profil pour chaque personne
  que la photo atteint&#160;: c'est ainsi
  que quelqu'un qui ne vous connaît pas voit un nom et un visage à côté. Toute
  copie de ce genre détenue par la personne que vous avez bloquée est détruite,
  et toute copie de la sienne que vous déteniez. Et comme le téléphone de cette
  relation ne sait rien du blocage et en enveloppera une autre à la prochaine
  photo, nous refusons aussi de remettre à l'un l'image ou la fiche de personne
  de l'autre tant que le blocage tient, quelles que soient les copies qui
  existent.
- **Vos mots sortent des publications de l'autre, dans les deux sens.**
  Réactions supprimées, commentaires retirés, définitivement. Après un blocage
  aucun des deux ne peut atteindre les publications de l'autre, donc un
  commentaire laissé là serait un commentaire que son propre auteur ne peut
  jamais supprimer – et des mots que vous ne pouvez pas reprendre sont des mots
  que vous n'avez pas accepté de laisser derrière vous.
- **Les demandes en cours dans un sens ou dans l'autre sont annulées**, sans
  quoi un blocage laisserait une invitation vivante de quelqu'un que vous
  venez de bloquer.

Ce qu'un blocage ne fait délibérément pas, c'est vous sortir l'un ou l'autre de
l'album d'une tierce personne. La pièce est la sienne, y être est un fait sur
la pièce plutôt que sur vous deux, et un blocage n'est pas un pouvoir sur
l'album de quelqu'un d'autre. Les deux noms restent sur sa liste de membres –
mais plus aucune photo ne passe entre vous là-bas.

Il ne retire pas non plus votre nom d'une photo publiée par une tierce
personne. Si une relation que vous avez en commun vous y a nommé, la photo est
la sienne, elle reste dans le fil de la personne bloquée, et votre pseudo
reste dessous. Ce qui s'en va, c'est tout ce que ce pseudo ouvrait. Votre
propre nom, vous pouvez toujours le retirer vous-même, depuis *options* sur la
photo, sans la permission de personne et sans blocage.

### Ce que la personne bloquée voit

Un «&#160;introuvable&#160;», partout. La recherche, l'envoi d'une demande,
votre profil, une de vos publications, l'adresse d'une photo, votre clé, votre
image, votre fiche de personne&#160;: chacun répond exactement ce qu'il répond
pour un compte qui n'existe pas, et rien de ce que ces portes lui remettent ne
vous identifie. À partir de ce qui vous concerne, elle ne peut donc pas
distinguer un blocage d'un compte qui n'a jamais été créé, et c'est le but.

La limite honnête est celle du paragraphe précédent&#160;: une pièce qui
appartient à quelqu'un d'autre dit toujours ce qu'elle disait. Votre pseudo
reste sur la liste de membres de l'album d'une tierce personne et sur une
photo à elle qui vous nomme, et un nom qui ouvrait une fiche et qui ouvre
maintenant un «&#160;introuvable&#160;», quelqu'un pourrait le remarquer.

### Défaire un blocage

Les gens que vous avez bloqués sont au bas de l'écran des personnes sous
*bloqués*, chacun un pseudo et *débloquer*. Le nom n'est pas un lien, parce que
plus rien n'ouvre son profil et qu'un lien vers un «&#160;introuvable&#160;»
est pire qu'un mot.

Le dialogue est titré *débloquer* et son pseudo, et il est honnête sur ce qu'un
déblocage est et n'est pas&#160;: *Cette personne pourra vous trouver et vous
redemander. Rien de ce qui a été retiré ne revient.* Le pseudo et non un nom,
pour la raison de la ligne&#160;: plus rien n'ouvre son profil pour en lire un.

Il n'y a pas de liste de qui vous a bloqué, et il ne peut pas y en avoir&#160;:
ce serait le signal que l'«&#160;introuvable&#160;» existe pour retenir.

## Signaler quelqu'un

*options → signaler*, sur un profil ou sur la ligne d'une demande reçue. Nous
ne détenons que du chiffré et ne pouvons voir ni la photo ni les mots, donc ce
qui nous parvient est un pointeur et le paragraphe que vous écrivez, qui voyage
en clair – le dialogue le dit. La personne signalée n'apprend jamais qu'un
signalement existe ni qui l'a déposé, et il ne vous est donné aucun numéro de
suivi, parce qu'une file qui promet une réponse est une file qui en doit une.
Tout ce que nous pouvons faire agit sur le compte plutôt que sur une photo. La
[politique de modération](/moderation/) en est la version longue.

Rien de l'état de votre propre compte ne vous empêche de signaler, une
suspension comprise&#160;: quelqu'un qui subit du harcèlement doit toujours
pouvoir le dire. La seule limite est un rythme – seize signalements par heure,
ce qui est une personne passant une mauvaise soirée plutôt qu'un script – et,
comme pour la limite de recherche, le refus ne récite pas le nombre.

## Ce qui n'est pas là

- **Pas d'annuaire et pas de suggestions.** Rien ne parcourt les comptes, rien
  ne calcule qui vous pourriez connaître, rien n'est classé.
- **Pas de profil public.** Demander les publications de quelqu'un avec qui
  vous n'êtes pas en relation est un «&#160;introuvable&#160;» et non une page
  vide – la même réponse pour un inconnu, pour vous-même, et pour un
  identifiant n'appartenant à personne. Il n'y a pas d'adresse de profil, pas
  de code QR et pas de «&#160;partager mon profil&#160;».
- **Pas de compteurs d'abonnés ou d'abonnements**, et pas de compteur de
  publications. Rien ne totalise ce que vous avez fait, et rien ne compte qui
  l'a vu. Ce qui est compté à la place est petit et privé&#160;: votre nombre
  de relations face à la limite, combien de personnes sont dans un groupe que
  vous avez fait, et combien de publications non vues un onglet d'accueil ou un
  album retient.
- **Aucun moyen de voir les relations de quelqu'un d'autre.** Le plus que vous
  appreniez jamais est *vous connaissez tous les deux…*, et chaque nom de cette
  ligne est déjà le vôtre.
- **Aucun moyen de voir qui vous a bloqué**, et aucun moyen d'apprendre dans
  lequel des groupes de quelqu'un vous êtes – l'appartenance à un groupe est
  invisible même pour les gens qui y sont.
- **Personne n'apprend qui a regardé.** Ni une demande, ni une photo. Un accusé
  de lecture par personne a été construit une fois puis retiré.
- **Pas d'invitation à distribuer.** Pendant la bêta, les codes viennent de
  nous et rien dans l'application n'en fabrique.

La [politique de confidentialité](/privacy/) dit exactement ce que nous
détenons sur vos relations et ce que nous ne pouvons pas voir, et [comment ça
marche](/fr/comment-ca-marche/) est le reste de ces pages.
