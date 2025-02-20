# Progressive Web Apps : The Future of the Mobile Web (Volume 2) – Traduction Complète

---

## Avant-propos

1. **Progressive Web Apps Installables**  
   - Le Web possède deux superpuissances distinctives  
   - La combinaison des superpuissances du Web et des applications natives  
   - Installation depuis le navigateur  
   - Installation depuis les boutiques d’applications  

2. **Stratégies produits pour les Progressive Web Apps**  
   - Stratégie 1 : Tout miser sur le Web  
   - Stratégie 2 : Compléter le natif avec une « Lite App »  
   - Stratégie 3 : Des applications séparées pour des tâches distinctes  
   - Stratégie 4 : Faible friction, base d’utilisateurs installés élevée  

3. **Exigences pour l’installabilité**  
   - Exigences pour une Progressive Web App installable  
   - Publication sur Play via Trusted Web Activities  

4. **Schémas de promotion de l’installation de PWA depuis le navigateur**  
   - Chrome sur Android  
   - iOS  
   - Desktop  

5. **Conception d’expériences installées**  
   - Expérience utilisateur (UX) d’installation  
   - Interface autonome (Standalone UI)  

6. **Conception d’expériences fiables**  
   - Principes centrés sur l’utilisateur pour le mode hors ligne  
   - Informer sur le changement d’état  
   - Fournir une expérience hors ligne  

7. **Conception d’expériences de notification significatives**  
   - Demander la permission  
   - Envoyer des notifications  

8. **Mesure de l’impact**  
   - Mesurer les taux d’installation  
   - Mesurer les utilisateurs installés  
   - Mesurer le mode hors ligne et la mise en cache  
   - Suivi de l’utilisation et des événements en Trusted Web Activity  
   - Mesurer les notifications push  

9. **Études de cas**  
   - Weekendesk  
   - Etam  

— Conclusion  
— Ressources et Outils

---

## Texte de l’avant-propos

**PW A:  
Les Superpuissances du Web  
&  
Apps Natives Combinées**

Le web est littéralement présent partout : sur les montres, smartphones, tablettes, ordinateurs, voitures, télévisions et panneaux numériques. Grâce aux navigateurs, le logiciel qui affiche le contenu web sur tous ces appareils et dans toutes ces tailles d’écran peut être exactement le même.

Même si les navigateurs restent au cœur de l’expérience utilisateur, chaque appareil dispose désormais de sa propre boutique d’applications, ce qui a modifié les habitudes. Sur Android, Chrome OS, Mac ou Windows, les utilisateurs ont appris que la boutique de leur appareil était l’endroit où ils pouvaient installer des logiciels conçus spécialement pour celui-ci.

L’essence même d’un logiciel installé repose sur l’engagement qu’il s’intègre à l’appareil de la manière attendue par l’utilisateur. Cette intégration facilite le lancement ultérieur du logiciel, par exemple via une icône sur l’écran d’accueil ou dans le menu Démarrer. Cela permet également à l’utilisateur de basculer entre les applications grâce au sélecteur d’activités intégré (comme « alt-tab » sous Windows ou le sélecteur d’applications sur mobile).

Les Progressive Web Apps (PWA) combinent la portée et la capacité de partage du web avec les intégrations natives attendues par les utilisateurs. Une PWA peut être découverte et installée sur n’importe quel appareil disposant d’un navigateur moderne, aussi bien sur mobile que sur desktop, et même dans des boutiques telles que Google Play. Quelle que soit la manière dont elle est découverte, si le logiciel offre une utilité répétable et une excellente expérience, l’utilisateur peut choisir de l’installer et d’intégrer cette expérience à son appareil – exactement comme n’importe quelle autre application.

*Par PJ McLachlan*

---

## Chapitre 1 – Progressive Web Apps Installables  
*Par Daniil Matveev*

**Le web possède deux superpuissances distinctives**

1. **La portée la plus étendue**  
   Le web touche tous les types d’appareils et de tailles d’écran.

2. **Les liens**  
   Les URL permettent l’indexation par les moteurs de recherche pour une découverte organique ainsi qu’un partage aisé de contenus et de services entre utilisateurs.

Ces superpuissances ont rendu le web incontournable comme plateforme sur desktop. Par exemple, des applications et suites de productivité telles que G Suite de Google, Microsoft Office 365, Trello, Slack, Discord, InVision ou Lucidchart existent depuis longtemps en tant qu’applications web de bureau.

Pourtant, sur mobile, ce sont souvent les boutiques d’applications natives qui sont perçues comme la référence, tant par les utilisateurs que par les développeurs. Pourquoi ? Autrefois, de nombreuses fonctionnalités nécessitant une intégration poussée au système d’exploitation n’étaient pas disponibles sur le web.

Aujourd’hui, le web prend en charge nativement presque toutes les fonctionnalités dont une application peut avoir besoin, notamment :

- L’accès aux médias et au streaming, ainsi que la capture de photos et de vidéos depuis n’importe quelle caméra de l’appareil  
- La détection de formes, incluant la lecture de codes-barres et la détection de visages  
- Les notifications push  
- L’authentification biométrique (reconnaissance faciale et empreintes digitales)  
- Le Bluetooth et le NFC  
- L’accès natif aux contacts  
- L’accès au système de fichiers de l’appareil  
- L’accès direct au presse-papiers  
- La détection du mouvement et de l’orientation de l’appareil, la vibration, l’orientation d’écran (avec verrouillage)

…et bien plus encore. Pour consulter la liste complète des fonctionnalités en développement, jetez un œil au projet Web Capabilities (Fugu).

**La combinaison des superpuissances du Web et des applications natives**

Les Progressive Web Apps combinent la portée et la capacité de partage du web avec les intégrations natives attendues par les utilisateurs. De nombreuses entreprises exploitent déjà les PWA pour offrir d’excellentes expériences. Par exemple :

- Des applications de taxi (comme Ola Cabs, Lyft ou Uber) utilisent les notifications push web pour informer les passagers du statut de leur course.  
- Des détaillants et des banques adoptent la navigation hors ligne pour ces moments « Oups, je croyais qu’il y avait du Wi-Fi dans le train… »  
- Des services de livraison, tels que Delivery Club, déploient des PWA grâce à leur facilité de maintenance et leur disponibilité sur plusieurs plateformes.

Une PWA peut être découverte dans le navigateur et utilisée immédiatement. Son contenu peut être partagé via une URL, accessible même si l’application n’est pas installée. Si l’utilisateur le souhaite, il peut installer la PWA et bénéficier des intégrations natives attendues, telles que :

- Un accès depuis des surfaces familières (écran d’accueil, tiroir d’applications)  
- Une expérience autonome, distincte du navigateur  
- L’accès aux services natifs (sélecteur d’applications, paramètres)

De plus, outre l’installation depuis le navigateur, une PWA peut être installée via des boutiques d’applications comme Google Play, Samsung Galaxy Store ou le Microsoft Store sur Windows 10.

Pour l’instant, ce chapitre vous présente un aperçu de l’expérience d’installation depuis le navigateur (sur mobile et desktop) ainsi que depuis les boutiques d’applications. Les chapitres suivants détailleront les exigences techniques (« Exigences pour l’installabilité ») et les schémas de conception pour promouvoir l’installation d’une PWA.

---

## Chapitre 2 – Stratégies Produit pour les Progressive Web Apps  
*Par Daniil Matveev*

Les entreprises rapportent souvent que les utilisateurs d’applications natives sont les plus précieux et fidèles, affichant une valeur à vie (LTV) supérieure à celle des utilisateurs web.  
Les expériences natives sont-elles vraiment supérieures aux expériences web, ou est-ce simplement que les utilisateurs les plus fidèles sont plus enclins à installer une application ? Les données recueillies auprès de diverses entreprises dans le monde tendent à confirmer cette seconde hypothèse.

La boutique de mode en ligne **ABOUT YOU** a déployé une Progressive Web App et proposé l’installation depuis le navigateur, en complément de leur application native disponible sur le Play Store. Ils ont constaté que les utilisateurs qui installent la PWA « génèrent des ventes cinq fois supérieures à celles de l’utilisateur mobile moyen » et qu’ils « se comportent de manière similaire aux utilisateurs de notre application native ».

Les Progressive Web Apps peuvent offrir une excellente expérience aux utilisateurs qui, autrement, n’installeraient jamais une application native. Les PWAs installées pèsent généralement moins de 1 Mo, ce qui est bien inférieur à la taille moyenne d’une application native. Par ailleurs, développer pour le web permet de supporter plus facilement la grande diversité de tailles d’écran et de capacités d’appareils.

Ces caractéristiques sont particulièrement importantes pour les entreprises visant une croissance sur des marchés émergents, où les forfaits de données sont onéreux, l’espace de stockage limité et les appareils parfois peu performants.  
Dans les marchés développés, bien qu’il existe une large gamme d’appareils et davantage d’utilisateurs possédant des smartphones haut de gamme, l’espace de stockage demeure un critère déterminant : plus on en dispose, plus on a tendance à l’utiliser. Ainsi, dans ces marchés, une PWA peut venir compléter une application native, notamment pour les utilisateurs qui désinstallent cette dernière pour libérer de l’espace.  
Rappelons qu’il existe, même dans les marchés développés, un grand nombre d’utilisateurs équipés d’appareils de gamme moyenne à basse. Une PWA permet donc de toucher l’ensemble de ces segments de manière rentable.

Tout en reconnaissant les avantages offerts par les PWAs, les entreprises peuvent demeurer interrogées sur la meilleure façon de les déployer pour compléter leurs applications natives existantes.  
Les quatre stratégies suivantes illustrent comment des entreprises aux besoins variés peuvent utiliser les PWAs pour offrir la meilleure expérience possible au plus grand nombre d’utilisateurs, tout en maîtrisant les coûts.

### Stratégie 1 : Tout miser sur le Web

**Pour les entreprises qui :**
- N’ont pas d’application native  
- Ont une application native de mauvaise qualité  
- Ont une application native reposant fortement sur du contenu web

**Développement :**  
- Créer une PWA  
- Publier la PWA sur le Play Store en utilisant Trusted Web Activities (TWA) – solution souvent la plus économique pour les entreprises axées sur le web qui souhaitent s’étendre dans le Play Store

**Promotion :**  
- Navigateur : Promouvoir l’installation de la PWA auprès de tous les utilisateurs  
- Play Store : Publier la PWA via TWA

**Avantages :**  
- Permet aux entreprises dépourvues d’application Android d’offrir une expérience installable  
- Peut remplacer une application Android obsolète, peu mise à jour ou offrant une mauvaise expérience (il est d’ailleurs particulièrement aisé de remplacer une application hybride dépassée par une PWA)  
- Consolide le développement mobile autour d’une unique base de code

**Inconvénients :**  
- Ne convient pas si des fonctionnalités spécifiques, non disponibles sur le web, sont requises

---

### Stratégie 2 : Compléter le natif avec une « Lite App »

Les termes « Lite » et « Go » ont été inventés pour distinguer l’expérience web, plus légère et plus rapide, de celle d’une application native, pour les entreprises souhaitant proposer les deux solutions.  
Pour les entreprises disposant déjà d’une excellente application native, une PWA sous l’appellation « Lite » peut permettre d’atteindre des utilisateurs qui n’installeraient jamais l’application native (par exemple, ceux équipés d’appareils de gamme moyenne ou basse).

**Développement :**  
- Créer une Progressive Web App  
- Publier la PWA sur le Play Store via TWA, en utilisant le suffixe « Lite » pour la différencier de l’application native  
- Développer également des applications natives

**Promotion :**  
- Navigateur : Promouvoir l’installation de l’application native ; en cas de refus, proposer la version PWA avec une proposition de valeur axée sur la version « Lite »  
- Play Store : Publier la PWA via TWA en utilisant la dénomination « Lite » pour que l’utilisateur puisse choisir son expérience préférée

**Avantages :**  
- Idéale pour les entreprises possédant une application Android performante mais « lourde », souhaitant offrir une meilleure expérience aux utilisateurs d’appareils de milieu ou bas de gamme, ou dans des zones à connectivité limitée

**Inconvénients :**  
- Nécessite la gestion de deux listings sur le Play Store et l’usage d’analyses pour segmenter intelligemment les utilisateurs afin de promouvoir la PWA ou l’application native via le navigateur

---

### Stratégie 3 : Des applications séparées pour des tâches distinctes

Pour de nombreuses entreprises, une PWA peut offrir l’expérience principale visant les objectifs de conversion, tandis qu’une application native pourra fournir des services complémentaires spécifiques à certains cas d’usage et offrir des fonctionnalités spécialisées.

*Exemples :*  
- Un détaillant peut proposer l’expérience principale d’achat via une PWA, et une application native distincte pour le contenu magazine ou lifestyle  
- Une compagnie d’assurance peut offrir les informations et la génération de leads via une PWA, et une application native séparée pour un chatbot, un service d’assistance ou de support client

**Développement :**  
- Créer une Progressive Web App  
- Publier la PWA sur le Play Store via TWA  
- Développer et maintenir également des applications natives à valeur ajoutée

**Promotion :**  
- Navigateur : Promouvoir la PWA à l’ensemble des utilisateurs. L’application native spécialisée sera proposée uniquement aux utilisateurs ayant atteint certains objectifs de conversion et susceptibles de bénéficier des fonctionnalités supplémentaires  
- Play Store : Avoir des entrées distinctes pour la PWA (publiée via TWA) et pour l’application native spécialisée, en précisant clairement dans chaque listing ce qui est proposé

**Avantages :**  
- Idéale pour les entreprises dont les objectifs de conversion sont simples et qui ne nécessitent une application native que pour des services de niche

**Inconvénients :**  
- Moins adaptée pour les entreprises n’offrant pas de services à forte valeur ajoutée

---

### Stratégie 4 : Faible friction, base d’utilisateurs installés élevée

Pour les entreprises capables d’offrir une expérience similaire entre l’application native et la PWA, une manière d’augmenter la base totale d’utilisateurs installés est de réduire au maximum la friction lors de l’installation.

- Depuis le navigateur, l’installation d’une PWA requiert seulement deux tapotements et n’oblige pas l’utilisateur à quitter le navigateur.  
- Dans le Play Store, avec un unique listing pour l’application native, l’utilisateur n’a pas à choisir entre différentes versions.

**Développement :**  
- Créer une Progressive Web App  
- Développer également des applications natives

**Promotion :**  
- Navigateur : Promouvoir la PWA auprès de tous les utilisateurs, à l’exception de ceux qui ont déjà installé l’application native (astuce : utiliser l’API `getInstalledRelatedApps` pour ne proposer l’installation de la PWA qu’aux utilisateurs dépourvus de l’application native)  
- Play Store : Ne proposer qu’un seul listing pour l’application native

**Avantages :**  
- Permet de réduire la friction d’installation, la PWA offrant un tunnel d’installation court sans nécessiter de quitter le navigateur, et un listing unique sur le Play Store évitant à l’utilisateur de devoir choisir entre plusieurs offres

**Inconvénients :**  
- La migration des utilisateurs de la PWA vers l’application native peut s’avérer complexe en l’absence de différenciation significative entre les deux produits  
- Les utilisateurs d’appareils de gamme moyenne ou basse qui découvrent l’application via le Play Store pourraient être réticents à l’installation en raison de préoccupations liées à l’espace de stockage ou à la compatibilité  
- Nécessite de maintenir simultanément la PWA et l’application native, surtout lorsqu’il existe peu de différences en termes d’expérience  
- Les coûts pourraient être réduits en optant pour une approche « Tout sur le Web » (Stratégie 1)

---

## Chapitre 3 – Exigences pour l’Installabilité  
*Par Martin Schierle*

**Exigences pour une Progressive Web App Installable**

Les exigences de base pour qu’une Progressive Web App soit installable sont les suivantes : être servie via HTTPS, disposer d’un service worker et inclure un manifeste d’application web.

### Servie via HTTPS

Nous sommes en 2020. Tous les sites devraient utiliser HTTPS, qu’ils soient des PWAs ou non !

### Service Worker

Les service workers constituent la technologie fondamentale des fonctionnalités des PWAs. Ils permettent d’effectuer des actions puissantes telles que la mise en cache et l’offre d’expériences hors ligne. Même si les exigences varient selon les navigateurs, il est fortement recommandé de disposer au minimum d’un service worker opérationnel avec un gestionnaire de requêtes (fetch handler).

### Manifeste d’Application Web

Le fichier manifeste est un document JSON qui indique comment la PWA doit se comporter une fois installée. Il doit être lié à chaque page pour que l’utilisateur puisse initier l’installation à tout moment. La plupart des navigateurs modernes le supportent à un certain niveau.

Le manifeste doit comporter :

- **short_name et name :**  
  Le `short_name` est utilisé sur l’écran d’accueil, dans le lanceur ou dans tout autre espace restreint, tandis que le `name` est affiché lors de l’invite d’installation.

- **Icônes :**  
  Utilisées sur l’écran d’accueil, dans le lanceur d’applications, le sélecteur d’applications, l’écran de démarrage, etc. Chrome requiert une icône de 192x192 px et une autre de 512x512 px. Des tailles additionnelles (notamment 270x270 et 180x180 px) sont recommandées, et d’autres dimensions sont optionnelles pour ceux qui souhaitent obtenir des icônes parfaitement adaptées.

- **start_url :**  
  L’URL de démarrage de la PWA lorsqu’elle est lancée depuis l’écran d’accueil. Cela empêche l’application de démarrer sur la page où se trouvait l’utilisateur lors de l’installation.

- **display :**  
  Il est recommandé d’utiliser le mode `standalone`. Ce mode permet à la PWA de s’ouvrir indépendamment du navigateur, en offrant une apparence et une convivialité comparables à celles d’une application native.

D’autres éléments peuvent être inclus dans le manifeste, dont vous pouvez prendre connaissance ultérieurement. Le chapitre « Conception d’expériences installées » traitera des meilleures pratiques en matière d’UX concernant les icônes et le nommage.

### Apple Touch Icon

iOS fonctionne légèrement différemment. Lorsque les utilisateurs de Safari sur iOS installent une PWA, l’icône affichée est appelée « Apple touch icon ». Pour définir l’icône que la PWA doit utiliser, ajoutez une balise `<link rel="apple-touch-icon" href="/exemple.png">` dans le `<head>` de la page. Sans cette balise, iOS génère une icône en prenant une capture d’écran du contenu de la page, ce qui est moins soigné. Pour une expérience utilisateur optimale, les icônes iOS doivent être de 180x180 px ou 192x192 px, et l’arrière-plan ne doit pas être transparent.

### Audits

Utilisez Lighthouse pour exécuter des audits et identifier ce qui manque pour activer l’installabilité.

### Publication sur le Play Store via Trusted Web Activities

Grâce aux Trusted Web Activities (TWA), les Progressive Web Apps peuvent être intégrées à une application Android et publiées sur le Play Store. Les TWA doivent répondre aux critères d’installabilité définis par Lighthouse et se charger rapidement, avec un score de performance d’au moins 80. Elles doivent également respecter les politiques du Play Store, notamment en ce qui concerne les paiements, les achats in-app et autres biens numériques.

Pour en savoir plus sur la publication d’une PWA sur le Play Store en utilisant les TWA, ainsi que sur des outils comme Llama Pack et PWA Builder qui simplifient ce processus, n’hésitez pas à consulter les ressources associées.

---

## Chapitre 4 – Schémas de Promotion de l’Installation d’une PWA depuis le Navigateur  
*Par Anna Potanina*

La promotion de l’installation d’une Progressive Web App doit intervenir au moment opportun dans le parcours utilisateur. Il est recommandé de personnaliser visuels, messages et design afin d’harmoniser l’expérience avec l’identité de marque et les besoins du client. Pour consulter quels navigateurs supportent une expérience d’invite d’installation entièrement personnalisable, vous pouvez vous référer à [caniuse.com](https://caniuse.com).

### Chrome sur Android

Sur Chrome pour Android, il est possible de créer une interface d’invite d’installation entièrement personnalisée. Pour ce faire, il convient tout d’abord d’empêcher l’affichage par défaut de la mini barre d’information.

- **Mini barre d’information** :  
  Initialement prévue comme solution temporaire, elle apparaît dès que le site répond aux critères d’installabilité et aux mesures d’engagement, sans tenir compte du contexte.  
- **Solution personnalisée** :  
  Il est préférable de désactiver cette mini barre et de proposer une invite sur-mesure qui :  
  - Ressemble à une interface native  
  - Communique une proposition de valeur claire assortie d’éléments visuels  
  - Apparaît au moment opportun et peut être redéployée à différents moments du parcours utilisateur

### iOS

Sur iOS, les utilisateurs doivent installer la PWA via le menu du navigateur. Il est alors essentiel de guider l’utilisateur à travers ce processus avec une invite explicative qui détaille les étapes à suivre.

### Desktop

Sur desktop, les Progressive Web Apps peuvent être installées via Chrome et Edge, quel que soit le système d’exploitation (Chrome OS, Linux, macOS, Windows).

- Une icône d’installation apparaît dans la barre d’adresse (omnibox) dès que le site est considéré comme installable, et cette icône peut se mettre en surbrillance pour attirer l’attention de l’utilisateur.
- Il est recommandé d’ajouter des indications visuelles pour informer l’utilisateur de cette possibilité.

### Bonnes Pratiques pour une Invite Personnalisée

- **Apparaître au Moment Opportun** :  
  Ne sollicitez pas l’installation dès la première visite. Attendez que l’utilisateur ait interagi de manière significative (par exemple, après avoir consulté un contenu clé ou lors de sa deuxième visite).

- **Utiliser une Proposition de Valeur** :  
  Mettez en avant les bénéfices pour l’utilisateur plutôt que de simplement énumérer les caractéristiques techniques. Par exemple :  
  *« Installez notre application web gratuite pour accéder rapidement à vos favoris. »*

- **Intégrer l’Invite dans l’Interface** :  
  Au lieu d’utiliser des pop-ups intrusifs, intégrez l’invite dans l’interface (par exemple dans le tiroir latéral ou l’en-tête de navigation), de façon à ce qu’elle soit toujours accessible sans interrompre l’expérience.

- **Utiliser des Visuels Appropriés** :  
  Des icônes et illustrations (comme une icône de téléchargement ou un bouton d’installation) renforcent le message et aident l’utilisateur à comprendre l’action attendue.

---

## Chapitre 5 – Conception d’expériences installées  
*Par Anna Potanina*

Concevoir une excellente expérience PWA qui réponde aux attentes d’une application installée s’appuie sur des pratiques déjà connues issues du web et du natif. Il est important d’écouter les utilisateurs et de tester régulièrement ses idées de design.

### Expérience d’Installation (Install UX)

La conception d’une PWA installée commence dès le choix du nom et de l’icône. Une fois installée, la PWA apparaît comme n’importe quelle autre icône sur l’écran d’accueil. Si vous disposez également d’une application native, il est important de les différencier, notamment par les icônes et le nom.

#### Icônes

- **Android** :  
  Envisagez de concevoir des icônes « maskable » qui s’adaptent aux formes requises par les fabricants.
  
- **iOS** :  
  Suivez les directives habituelles de design des icônes. Notez qu’iOS n’utilise pas l’icône définie dans le manifeste, d’où la nécessité d’ajouter une balise `<link rel="apple-touch-icon" ...>` dans le `<head>`.

#### Nommage

Utilisez le nom de l’entreprise comme nom de la PWA. Si la PWA utilise des domaines locaux (par exemple, example.co.uk ou example.fr), pensez à inclure la mention du pays dans le nom. L’ajout d’un suffixe « Lite » peut également aider à distinguer la PWA de l’application native lorsque les deux coexistent.

#### Lancement

Au lancement depuis l’écran d’accueil, Android affiche par défaut un écran blanc jusqu’à ce que la PWA soit chargée (ce qui peut durer jusqu’à 200 ms). Pour adoucir cette transition, il est possible de personnaliser l’écran de démarrage (splash screen). Chrome pour Android gère automatiquement cette personnalisation si le manifeste contient :
- La propriété `name`
- Une propriété `background_color` avec une valeur CSS valide
- Une icône dans le tableau `icons` d’au moins 512×512 px, au format PNG

Sur iOS, l’écran de démarrage ne peut pas être personnalisé de la même manière, et il faut utiliser des balises meta pour définir des écrans pré-générés.

---

## Chapitre 6 – Conception d’expériences fiables  
*Par Anna Potanina*

Fournir une expérience hors ligne dans une Progressive Web App signifie offrir à l’utilisateur une expérience conforme à ce qu’il attend d’une application native, même en l’absence de connexion : l’interface reste accessible et des messages d’erreur clairs sont affichés en cas de problèmes de connectivité.

### Fournir une Expérience Hors Ligne

Lors de la conception de l’expérience hors ligne, appliquez des méthodes de design thinking pour déterminer quelles fonctionnalités hors ligne pourraient réellement bénéficier à l’utilisateur.  
Quelques questions pour stimuler la réflexion :
- Comment pourrions-nous utiliser les données de localisation pour personnaliser l’expérience hors ligne ?
- Comment pourrions-nous stimuler des conversions multi-appareils en tirant parti des opportunités hors ligne ?
- Comment pourrions-nous exploiter le contenu de marque pendant que l’utilisateur est hors ligne ?
- Comment pourrions-nous maintenir la cohérence entre l’expérience hors ligne et celle en ligne ?
- Comment pourrions-nous offrir des options de support tout en maintenant l’engagement sur la page ?

### Principes Centrés sur l’Utilisateur pour le Hors Ligne

La connectivité n’est pas binaire (en ligne/hors ligne) mais peut fluctuer. Sur mobile, par exemple, l’utilisateur peut être dans un métro, un ascenseur ou dans une zone de couverture faible. Offrir une expérience robuste hors ligne permet de maintenir l’engagement, quelle que soit la qualité de la connexion.

### Informer de la Changement d’État

Il est essentiel d’informer l’utilisateur du changement d’état à l’aide de :
- **Texte** : Messages clairs et simples (ex. : « Vous êtes actuellement hors ligne »).
- **Icônes** : Visuels explicites illustrant le statut.
- **Couleurs** : Teintes indiquant que certaines zones sont en mode hors ligne.

Il est recommandé d’utiliser au moins deux de ces éléments pour éviter toute confusion.

### Expériences Hors Ligne Proposées

- **Fallback** : Afficher une page statique avec des alternatives (formulaire de contact, localisateur de magasins, informations clés, etc.).
- **Accès aux données personnelles** : Permettre l’accès à des éléments tels que billets, cartes d’embarquement, ou articles sauvegardés.
- **Divertissement** : Proposer un jeu, un puzzle ou des anecdotes pour occuper l’utilisateur pendant la coupure de connexion.

### Navigation et Tâches Hors Ligne

- Utilisez la mise en cache (pré-mise en cache et run-time caching) pour permettre à l’utilisateur de continuer à naviguer.
- Permettez à l’utilisateur d’effectuer des actions importantes (ajouter au panier, remplir un formulaire) et assurez-vous que ses actions soient conservées et traitées dès le rétablissement de la connexion.

### Indiquer le Changement d’État via une Interface

Utilisez un composant comme un toast ou snackbar pour notifier l’utilisateur, avec une action rapide (ex. : « Actualiser »). Assurez-vous que ce composant ne bloque pas les éléments de navigation.

---

## Chapitre 7 – Conception d’expériences de notifications significatives  
*Par Anna Potanina*

Les Progressive Web Apps supportent les notifications push sur Android, qu’elles soient installées ou non par l’utilisateur. Ces notifications peuvent accroître l’engagement et stimuler les ventes, mais une mauvaise gestion peut nuire à l’image de l’application.

### Demander la Permission

- Ne demandez pas la permission dès la première visite.  
- Sollicitez-la au moment opportun, lorsque l’utilisateur peut percevoir la valeur ajoutée des notifications.  
- Utilisez une interface préliminaire personnalisée (texte, visuels, style) pour préparer la demande.
- Assurez-vous que l’invite reste accessible sur l’ensemble du site, par exemple dans le menu latéral ou l’en-tête.

### Proposition de Valeur

Adaptez le message en fonction du contexte. Par exemple, sur une page produit, le message pourrait être :  
*« Recevez une notification lorsque cet article est de nouveau en stock. »*

### Envoi des Notifications

Chaque notification doit être :
- **Opportune, précise et pertinente**  
  Le message doit être clair, concis (moins de 40 caractères par élément de texte) et spécifique à l’utilisateur.
- **Composée de trois éléments** :
  - **Texte (Copy)** : Incluant le nom de la PWA, le titre et le contenu du message.
  - **Visuels** : Icône de la PWA ou images complémentaires (sans redondance).
  - **Actions (optionnel)** : Permettre à l’utilisateur d’interagir directement (sans dupliquer les actions natives d’Android).

---

## Chapitre 8 – Mesure de l’impact  
*Par Martin Schierle*

Une Progressive Web App bien conçue doit augmenter l’engagement, accélérer le chargement des pages et stimuler les conversions. Pour mesurer cet impact, il est recommandé d’évaluer séparément chaque fonctionnalité :

### 1. Mesurer les Taux d’Installation

- **Sur Chrome et Edge** :  
  - Nombre d’utilisateurs éligibles à l’installation (via l’événement `beforeinstallprompt`)  
  - Nombre de clics sur l’invite d’installation personnalisée  
  - Nombre d’utilisateurs acceptant ou refusant l’invite (via la propriété `userChoice`)  
  - Nombre d’installations effectives (via l’événement `appinstalled`)
  
- **Pour les autres navigateurs (ex. Safari)** :  
  Suivre l’utilisation de la PWA installée via des indicateurs spécifiques.

### 2. Mesurer les Utilisateurs Installés

- Ajouter un paramètre de suivi dans l’URL de lancement défini dans le manifeste.
- Détecter dynamiquement le mode autonome (standalone) pour distinguer le trafic provenant de la PWA installée.

### 3. Mesurer l’Utilisation Hors Ligne et la Mise en Cache

- Enregistrer les événements analytiques pendant la période hors ligne (via Workbox pour Google Analytics, par exemple).
- Suivre les événements de connexion/déconnexion (avec l’API `Navigator.onLine`) pour mesurer la durée hors ligne.

### 4. Suivi en Trusted Web Activity (TWA)

- Pour les PWAs publiées sur le Play Store via TWA, de nombreuses métriques (taux d’installation, engagement, etc.) sont disponibles dans la console du Play Store.
- Transmettre des paramètres de suivi pour analyser le comportement des utilisateurs dans la TWA.

### 5. Mesurer les Notifications Push

- Suivre le processus complet :  
  - Nombre d’utilisateurs éligibles (via feature detection)  
  - Nombre de clics sur l’invite personnalisée pour activer les notifications  
  - Nombre d’utilisateurs acceptant ou refusant la permission  
  - Pour chaque notification, mesurer le nombre d’événements push reçus et le taux d’engagement (clics, ouvertures via `notificationclick`, etc.)

Ces mesures permettent d’optimiser chaque étape du tunnel et d’identifier les points d’amélioration pour maximiser l’impact des PWAs.

---

## Chapitre 9 – Études de cas

Ce chapitre présente deux exemples concrets illustrant la mise en œuvre réussie des Progressive Web Apps.

### Weekendesk

Weekendesk, leader des séjours de week-end et des courts séjours thématiques (bien-être, gastronomie, détente, etc.), a transformé son site mobile en une Progressive Web App.  
Les résultats obtenus :
- Augmentation des conversions de 2,5 fois pour les utilisateurs accédant via la PWA installée.
- Accélération du chargement du site, jusqu’à 30 % plus rapide.
- Hausse de l’engagement, avec une augmentation de 108 % des pages vues et de 85 % du temps passé sur le site.

L’utilisation des service workers et la publication via Trusted Web Activities ont permis d’unifier le développement web et mobile.  
_Maxime Biloé, Lead Front Developer chez Weekendesk, explique :_  
« Nos utilisateurs attendent une expérience rapide et intuitive, quel que soit le canal. Notre choix gagnant a été de moderniser notre site en une Progressive Web App, puis de la publier également sur le Play Store. »

### Etam

Etam, spécialiste de la lingerie féminine, a choisi d’améliorer l’expérience mobile en développant une Progressive Web App, sachant que plus de 70 % des sessions proviennent de smartphones.  
Face à une application native vieillissante, l’équipe d’Etam a :
- Optimisé le code pour accélérer le chargement des pages.
- Mis en place une architecture permettant de mémoriser le contenu statique (espace client, etc.), afin de garantir l’accès à la carte de fidélité et à la liste de favoris même hors ligne.

Concernant l’installation de la PWA, une interface personnalisée a été conçue :
- **Avant l’installation** : Une invite sur la première tuile propose le message « Soyez le premier à connaître nos dernières actualités. Notre application est rapide, légère et fonctionne en mode hors ligne. »
- **Après installation** : L’expérience devient immersive grâce à une interface en plein écran, avec un design proche de celui d’une application native (ex. : menu de navigation en bas de l’écran).
