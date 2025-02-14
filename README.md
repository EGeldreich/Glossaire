# GLOSSAIRE

-   [Général](#général)
-   [Front-end](#front-end)
-   [UX / UI](#ux-ui)
-   [Architecture](#architecture)
-   [Modélisation / Base de données](#modélisation---base-de-données)
-   [Symfony](#symfony)
-   [Sécurité](#sécurité)
-   [RGPD](#rgpd)
-   [SEO](#seo)
-   [Gestion de projets / DevOps](#gestion-de-projets---devops)
-   [English](#english)

## Général

1. Quel est l’environnement à installer pour exécuter un script PHP ? Citer 2 exemples de logiciels permettant ce contexte

    > Il faut installer un serveur local. Laragon ou MAMP permettent d'en créer un

2. Qu’est-ce qu’un algorithme ?

    > Une suite d'odres à executer pour parvenir à un résultat

3. Qu’est-ce qu’une variable ? Par quel symbole est préfixée une variable en PHP ?

    > En PHP, une variable est un nom auquel on associe une valeur (pouvant prendre de nombreuse formes) qui peut varier. $nomDeMaVariable

4. Qu’est-ce que la portée d’une variable ?

    > La portée d'une variable représente à quels endroit elle peut être appelée, certaines variable ne sont définie qu'à l'intérieur d'une fonction par exemple.

5. Qu’est-ce qu’une constante ? Quelle est la différence avec une variable ?

    > Une constante est proche d'une variable - dans sa façon de la définir et sa portée - mais garde une valeur constante

6. Qu’est-ce qu’une superglobale, combien en existent-ils et donner un exemple d’utilisation

    > Une superglobale est une variable disponible par défault en PHP. Il en existe 8.  
    > $_GET $_POST $_COOKIE $_REQUEST $_SESSION $_FILES $_ENV $_SERVEUR  
  	> $\_SESSION['products'][] = $product; Ajoute un objet $product précédemment défini dans le tableau 'products' de la session de l'utilisateur

7. Quels sont les différents types (primitifs) que l’on peut associer à une variable en PHP ? Les citer et en donner des exemples (ne pas oublier le type d’une variable sans valeur)

    > Nombre entier (int) $a = 42;  
    > Nombre décimal (float) $a = 4.2;  
    > Chaine de caractères (string) $a = "hey";  
    > Booléen (boolean) $a = false;  
    > Tableau (array) $a = [ "a", "b"];  
    > Object (object) $a = new myClass;  
    > Vide (null) $a = null;

8. Existe-t-il plusieurs types de tableaux en PHP, si oui lesquels ?

    > Tableaux indéxés ( $tableau = ["elem1" , "elem2", ...]) dont les clés sont par défaut des chiffres, commencant à 0.  
    > Tableau associatif ( $tableau = [ "nom" => "Emmanuel", "age" => "31"] ) dont les clés sont des chaînes de caractères

9. Quelles sont les différentes structures de contrôles qu’il existe en algorithmie ? Donner un exemple pour chacune d’entre elles

    > Structure conditionnelle : Execute l'instruction si une condition est vérifiée (if)
    > Structure itérative : Repète une suite d'instruction un certain nombre de fois (foreach / for / while ...)

10. Quelle est la fonction PHP permettant de demander la longueur d’une chaîne de caractères ?

    > strlen(string $string): int

11. Qu’est-ce qu’une session ? Quelle fonction permet de démarrer une session en PHP ? Donner un exemple d’utilisation en PHP

    > session_start() crée une session ou reprend celle en cours
    > Une session permet de stocker des informations qui restent disponibles à travers plusieurs pages

12. Qu’est-ce qu’un cookie ? Donner un exemple d’utilisation en PHP

    > Un cookie est une variable stockée dans le navigateur, un peu comme une session mais qui ne se termine pas forcément à la fermeture du site
    > On peut par exemple stocké un cookie afin que le site se 'souvienne' du login (remember me)

13. Quelle est la différence entre les instructions « require » et « include » en PHP

    > Require et Include permettent de récupérer le contenu code d'un fichier A dans un autre fichier B. Cela permet de structurer son fichier de travail.
    > Ils sont identiques mis à part en cas d'echec, require produit une E_COMPILE_ERROR (fatal error qui arrete le script), alors qu'include produit un E_WARNING (warning et le script continue)

14. Comment effectuer une redirection en PHP ?

    > header('Location: http://www.example.com/');

15. Définir la partie « front-end » et « back-end » d’une application

    > La partie front-end englobe toute la partie visible d'une application, celle avec avec l'utilisateur interagit
    > La partie back-end est la partie 'cachée', dans laquelle se déroule la logique, comme l'interaction avec la base de donnée

16. Définir le contrôle de version ? Qu’est-ce que Git ?

    > Le contrôle de version est le fait de sauvegarder son travail sans écraser les versions précédentes. Cela permet de revenir à une version précédante si besoin.
    > Git est le VCS (version control system) lié à Github notament

17. Qu’est-ce qu’un CMS ? Citer au moins 2 exemples

    > CMS, Content Management System, est un outil qui accompagne dans la création d'application web.
    > Un CMS arrive souvent avec des thèmes pour la partie front-end, et un back-office déjà créé.
    > Wordpress, Drupal, Webflow

## Front-end

18. Définir HTML

    > HyperText Markup Langage, l'html est l'ossature d'un site web, son fond, le contenu lisible.

19. Définir CSS

    > Cascading Style Sheets, le CSS est la surcouche de décors par dessus l'html. Il sert à améliorer l'expérience utilisateur en créant une interface pratique.

20. Définir Javascript

    > Le javascript est le langage utilisé principalement pour ajouter de l'interactivité à un site, il vient généralement en renfort du CSS pour améliorer l'expérience utilisateur.

21. Définir JSON. Dans quel contexte ce format est-il utilisé ?

    > JavaScript Object Notation, le JSON est le principale langage utilisé lors de l'échange de données simples, par exemple lors de l'utilisation d'API

22. Peut-on interpréter du Javascript côté serveur ? Si oui, comment ?

    > Il est possible d'utiliser le langage JavaScript coté serveur, en utilisant Node.JS par exemple

23. Qu’est-ce qu’un sélecteur CSS ?

    > Un sélecteur CSS est ce qui définie ("sélectionne") les éléments qui seront affectés par le code qui lui est donné
    > .exemple { sélectionne tous les éléments ayant la classe exemple }

24. Quelle balise HTML permet de créer un lien hypertexte ?

    > <a href="adress.du.lien">Texte cliquable</a>

25. Qu’est-ce qu’une requête AJAX ?

    > Requête HTTP asynchrone qui met à jour des parties de la page sans nécessiter un rafraichissement

26. Quel sélecteur CSS permet de sélectionner tous les éléments d’une classe spécifique ? D’un identifiant spécifique ?

    > .classe{} #id{} type{}

27. Définir le responsive design

    > Le responsive design fait référence à la fléxibilité de l'interface d'un site lors du changement de la taille de l'écran.  
    > Un bon responsive design utilise des valeurs flexibles ( % par exemple ) et des breakpoints réfléchis à l'avance pour le changement du placement des éléments.

28. Qu’est-ce que le templating ?

    > Le templating est le fait de créer un élément (comme une nav, footer ...) dans un fichier à part, et de l'appeler sur les pages où il est nécessaire

29. Qu’est-ce qu’une fonction anonyme en Javascript ?

    > Un fonction anonyme est une fonction qui n'est pas nommé. C'est régulièrement le cas pour les fonctions qui sont utilisés dès leur création, comme dans un addEventListener par exemple

30. Quelle méthode JavaScript est utilisée pour ajouter un élément à la fin d'un tableau ?

    > tableau.push(element);

31. Qu’est-ce qu’un « media query » ?

    > Un media query est un "breakpoint" (point de bascule) utilisé en CSS pour définir des attributs qui deviennent valable dans certains cas, lorsque le breakpoint est activé.

32. Qu’est-ce qu’un pseudo élément en CSS ?

    > Un pseudo élément CSS est un élément qui n'existe pas en HTML mais qui est créé en CSS, par exemple ::before crée un ouvel élément avant l'élément selectionné

33. Qu’est-ce que Bootstrap ? Donner d’autres exemples équivalent

    > Bootstrap est une librairie CSS, qui permet d'ajouter à son HTML des classes pré-stylisées.
    > TailWind est équivalent dans son utilisation.

34. Quand un formulaire HTML est créé, quelles sont les 2 méthodes qui peuvent lui être associées ? Donner la différence entre ces 2 méthodes

    > method="POST" et method="GET".
    > POST stocke les données dans la session alors que GET les stocke dans l'URL.
    > POST est donc plus 'privatif' et moins sujet aux changements par l'utilisateur.

## UX UI

35. Quelle est la différence entre UX Design et UI Design ?

    > UX (experience utilisateur) concerne tout ce qui est lié à l'ergonomie d'un site (arborescence, affordance, interaction ...)  
    > UI (interface utilisateur) concerne l'interface elle même (typographie, couleurs)
    > Les deux sont liés, puisque l'UI fait partie de l'experience utilisateur

36. Qu’est-ce qu’un wireframe ?

    > Un wireframe est généralement la première étape pour poser un design, il s'agit de l'ossature, qui se concentre sur le placement des éléments et leur taille

37. Qu’est-ce qu’un prototype ?

    > Un prototype, en web, est une maquette poussée, avec les interactions visibles, ainsi que les liens entre les différentes pages

38. Qu’est-ce que la hiérarchie visuelle en UI Design ?

    > La hiérarchie visuelle est le fait que certains éléments doivent primer sur d'autres, car ils sont plus important.
    > On peut influencer la hiérarchie visuelle via la taille ou la couleur par exemple

39. Qu’est-ce que l’accessibilité en UX Design ?

    > L'accessibilité est la capacité (nécessité) pour un site d'être consulté par des personnes avec divers handicap physique (mauvaise vue, membre cassé ...) ou matérielle ( mauvaise connexion / pas de souris ...)

40. Qu’est-ce qu’une grille de mise en page ?

    > Une grille de mise en page est une grille que l'on utilise lors de la création de wireframes ou maquette pour s'assurer que les éléments soient placés correctement (alignés, même espacement ...)

41. Qu’est-ce que la notion d’affordance en UX Design ?

    > La notion d'affordance est à la capacité d'un élément à être compris clairement.
    > Le fait que le curseur change au survol d'un élément cliquable, ou l'utilisation d'icones répandues sont des éléments qui favorisent l'affordance

42. Qu’est-ce qu’un « mobile first design » ?

    > Un design mobile first est un design qui se concentre en premier lieu sur sa version réduite (mobile) puis qui pense sa version grand écran en second temps  
    > Cette méthode est souvent utilisé pour les sites / web apps qui visent une utilisation principalement sur mobile

## Programmation orientée objet (POO)

43. Donner une définition de la programmation orientée objet

    > La POO est une façon d'approcher le code particulière, dans laquelle on définit des objets avec lesquels il est possible d'interagit

44. Qu’est-ce qu’une classe ? Comment la déclare-t-on ?

    > Une classe est la structure d'un objet, dans la classe on définie le constructor (ce qui contient l'objet), et les méthodes accessible dans cet objet
    > class Voiture {}

45. Qu’est-ce qu’un objet ?

    > Un objet est une instanciation d'une classe
    > $mercedes = new Voiture()

46. Définir la notion de propriété / attribut / méthode

    > Propriété et attributs font tous les deux références à la même chose, les données que contient l'objet
    > Méthodes : Les méthodes sont les fonctions internes de l'objet

47. Qu’est-ce que la visibilité d’une propriété ou d’une méthode ? Citer les différents types de visibilité

    > La visibilité fait référence à la portée d'un attribut ou d'une méthode.
    > On distingue les éléments **private**, qui ne sont accessible qu'à l'interieur de la classe dans laquelle ils sont définis
    > Les **public** qui sont toujours accessible
    > Les **protected** qui sont accessible à l'interieur de la classe, et des classes liées (heritiers et parents)

48. Quelle est la méthode spécifique utilisée pour créer un nouvel objet à partir d’une classe ?

    > $mercedes = new Voiture()

49. Qu’est-ce que l’encapsulation ?

    > L'encapsulation est le fait de regrouper un ensemble de méthodes et de données dans une structure
    > Tout le système de POO est basé sur l'encapsulation

50. Que signifie « étendre une classe » ? Quelle est le concept clé mis en œuvre ? Donner un exemple

    > Etendre une classe signifie faire profiter des propriétés et méthodes d'une classe à un nouvelle
    > On parle également d'héritage
    > class Voiture extends Machine {}

51. Définir l’opérateur de résolution de portée

    > **::**

52. Définir une méthode / propriété statique

    > Des propriétés ou méthodes définient comme **static** sont accessibles sans avoir besoin d'instancier la classe
    > Voiture::nb_roue;

53. Définir le polymorphisme en POO

    > Le polymorphisme est un concept où des objets de différentes classes peuvent répondre de manièr différente aux mêmes actions
    > Il est par exemple possible de définir deux méthodes portant le même noms mais qui effectue une action différente en fonction de la classe

54. Définir une méthode / classe abstraite ?

    > Une classe **abstract** est une classe qui ne peut pas être instanciée
    > Une méthode abstaite est une méthode définie mais sans contenu. Une méthode ne peut être abstraite que dans une classe abstraite
    > Cela est utilisé pour l'héritage des classes

55. Définir le chaînage de méthodes

    > Le chaînage de méthodes est le fait de mettre à la suite plusieurs méthodes.
    > Cela peut par exemple être utilisé pour **_get_** des entités qui sont encastrés
    > $voiture->getRoue()->getPneu()->getMarque()

56. Qu’est-ce que la méthode \_\_toString() ? Existe-t-il d’autres méthodes « magiques »

    > La méthode **toString** permet de définir le string qui est renvoyé lors d'un echo de l'objet
    > Il existe de nombreuses méthodes magiques:
    > **construct(), **destruct(), **call(), **callStatic(), **get(), **set(), **isset(), **unset(), **sleep(), **wakeup(), **serialize(), **unserialize(), **toString(), **invoke(), **set_state(), **clone(), and \_\_debugInfo()
    > Ces méthodes change le comportement par défaut de PHP

57. Qu’est-ce qu’un « autoload » ?

    > Un autoload permet d'**_include_** automatiquement les fichiers dans lesquels sont définis les classes, afin d'éviter à devoir rajouter chaque classe manuellement

    ```php
    spl_autoload_register(function ($class_name) {
        include $class_name . '.php';
    });

    ```

58. Comment appelle-t-on en français les « getters » et les « setters » ?

    > **accesseurs** et **mutateurs**

59. Qu’est-ce que la sérialisation en PHP ?

    > La sérialisation transforme un objet ou structure en une chaine de caractères.
    > Cela permet de transferer l'objet ou la structure à un autre fichier par exemple.
    > **serialize()** // **unserialize()**
    > Un peu le même principe que JSON parse / stringify

## Architecture

60. Qu’est-ce que l’architecture client / serveur ? Grâce à quel type de requête peut-on interroger le serveur. Définir l’acronyme de ce type de requête. Si on ajoute un « S » à cet acronyme, expliquer la différence

    > L'architecture client / serveur est l'environnement qui met en relation les machines des utilisateurs (client) et les machines de type serveur
    > On intérroge généralement le serveur avec une requête GET
    > Ce type de requête appartient au protocole HTTP (HyperText Transfer Protocol)
    > HTTPS (Secure) combine l'HTTP à une couche de chiffrement pour le sécuriser

61. Donner la définition d’un design pattern. Citer au moins 3 exemples de design pattern

    > Un **_design pattern_** est une façon structurée d'organiser son code, pour permettre une expansion et un partage du code plus simple.
    > Les design pattern sont traditionnellement créés pour répondre à un problème réccurant
    > MVC Model View Controller
    > Factory
    > Singleton

62. Qu’est-ce que l’architecture MVC ?

    > L'architecture MVC (Model View Controller) est un structuration spécifique qui permet de bien séparer son code

63. Quel est le rôle de chaque couche du design pattern MVC : Model, View, Controller ?

    > Model : s'occupe des données (génération des entités et dialogue avec la BDD)
    > View : s'occupe de la génération des pages
    > Controller : s'occupe de la logique, c'est ici que se passe les redirections, la sécurité ...

64. Quels sont les avantages de l’architecture MVC ?

    > Facilité de modification et de gestion. Structure connue et logique qui permet une bonne passation du projet à d'autres développeurs

65. Existe-t-il des variantes à l’architecture MVC ?

    > Il existe de nombreuses variantes à l'architecture MVC, qui tentent de combler certaines lacunes
    > HMVC (Hierarchical)
    > MVP Model View Presenter
    > ...

66. Qu’est-ce qu’une API ? Définir l’architecture REST

    > Une API est un regroupement de données ordonnées, disponibles via des requêtes HTTP
    > Une API dispose d'un ou plusieurs **endpoint** qui permettent de récupérer ces données
    > https://pokeapi.co/api/v2/pokemon/ditto
    > REST REpresentationnal State Transfer, définit un ensemble de contraintes à utiliser pour créer des services web
    > il consiste en les **méthodes HTTP** **_GET, HEAD, POST, PUT, PATCH, DELETE, CONNECT, OPTIONS, TRACE_**,
    > un **URI** et un **type de média (type MIME)** (par exemple JSON)

## Modélisation - Base de données

67. Qu’est-ce que la modélisation de données ? Définir la méthode Merise

    > La modélisation de données est la création d'un modèle visuel représentant une base de donnée.
    > Cela permet de mieux visualiser les besoins avant de se lancer dans la création
    > La méthode Merise séparent un modèle en 3 niveaux ( Conceptuel **MCD**, Logique **MLD** et Physique **MPD** )

68. Quelles sont les 3 étapes principales de la méthode Merise ?

    > Analyse, conception et réalisation

69. Qu’est-ce qu’un modèle conceptuel de données (MCD) en Merise ?

    > Schéma représentant la structure du système d'information (dans notre cas généralement la base de donnée)
    > Met en avant les relations et les dépendances (**ManyToOne, OneToMany, ManyToMany** ...)

70. Qu’est-ce qu’un modèle logique de données (MLD) en Merise ?

    > Schéma représentant la structure du système
    > Précise la volumétrie, la structure et l'organisation des données (précise le type des données, place les clés étrangères)

71. Donner la définition des mots suivants :
    a. Entité

    > Une entité est un élément que l'on souhaite représenter dans sa base de donnée. **_USER_** **_COMMENT_** **_TEACHER_** ...
    > b. Relation
    > Lien entre les entités
    > c. Cardinalité
    > Type du lien, **_ManyToOne_** **_OneToMany_** ...
    > d. Clé primaire / clé étrangère
    > La clé primaire est l'identifiant unique de l'entité
    > La clé étrangère est la référence d'une clé primaire d'une autre table

72. Que devient une relation de type « Many To Many » dans le modèle logique de données ?

    > Un table associative

73. Qu’est-ce qu’une base de données ?

    > Ensemble ordonnée de données, sauvegardé sur un serveur

74. Définir les notions suivantes :
    a. SQL

    > Langage utilisé avec les bases de données, Structured Query Language
    > b. MySQL
    > Système de gestion de base de donnée
    > c. SGBD (donner 2 exemples de SGBD)
    > Un système de gestion de base de donnée est un logiciel permettant aux utilisateurs de créer et gérer des bases de données
    > MySQL, MongoDB, PostgreSQL ...

75. Dans une base de données, les données sont stockées dans des \_\_\_. Celles-ci sont constituées de lignes appelées \_\_\_ et de colonnes appelées \_\_\_

    > Tables
    > Entrées
    > Champs

76. Quelle est la différence entre une base de données relationnelle et non relationnelle ?

    > Une base de donnée relationnelle gère les relations entre les tables (à l'aide de clé étrangères), une non relationnelle ne comporte que des tables indépendantes (NoSQL)

77. Qu’est-ce qu’une jointure dans une base de données ? En existe-t-il plusieurs ? Si oui lesquelles ?

    > Une jointure permet, en SQL, de récupérer des infos à travers plusieurs tables
    > INNER JOIN retourne les entrées avec une condition (id = clé étrangère)
    > LEFT / RIGHT JOIN retourne les entrées de 2 tables en conservant l'intégralité de l'une d'elle, et seulement les entrées qui répondent à la condition de l'autre
    > FULL JOIN retourne toutes les entrées, mais avec une valeur nulle si la condition n'est pas remplie

78. A quoi sert une vue dans une base de données ?

    > Une vue dans une base de donnée est une requête enregistrée qui permet d'acceder aux données voulues plus simplement.
    > Cela permet de l'utiliser comme une table temporaire virtuelle

79. Qu’est-ce que l’intégrité référentielle dans une base de données ?

    > L'intégrité référentielle est la protection dans une base de données relationnelle qui empèche de supprimer un élément si celui ci à un lien avec une autre table
    > Il est possible de changer l'intégrité référentielle, par exemple en mettant en place des supression en **CASCADE**

80. Quelles sont les fonctions d’agrégation en SQL ?

    > COUNT()
    > SUM()
    > MIN() MAX()
    > AVG()
    > Une requête comprenant une fonction d'agrégation doit se terminer par un GROUP BY

81. Qu’est-ce qu’un CRUD dans le contexte d’une base de données ?

    > Create Read Update Delete
    > La capacité de créer, lire, modifier et supprimer une entrée

82. Quelles sont les clauses qui permettent de :
    a. Insérer un nouvel enregistrement dans une table

    > INSERT INTO table VALUES ('valeur 1', 'valeur 2', ...)
    > b. Modifier un enregistrement dans une table
    > UPDATE table SET nom_colonne = '...' WHERE ...
    > c. Supprimer un enregistrement dans une table
    > DELETE from table WHERE
    > d. Supprimer la base de données
    > DROP DATABASE ma_base
    > e. Filtrer les résultats d’une requête SQL
    > SELECT \* WHERE conditions du filtre
    > f. Trier les résultats d’une requête SELECT
    > SELECT ... ORDER BY 'colonne' ASC / DESC
    > g. Regrouper les résultats d'une requête SELECT en fonction d'une colonne spécifique
    > SELECT ... GROUP BY 'colonne'
    > h. Concaténer 2 chaînes de caractères
    > CONCAT(col1, ' ', col2) AS nouveauNom

83. Comment se connecter à une base de données en PHP ? Quelle est la classe native utilisée ?

    > On utilise la classe native PDO

    ```php
    public static PDO::connect(
        string $dsn,
        ?string $username = null,
        #[\SensitiveParameter] ?string $password = null,
        ?array $options = null
    ): static
    ```

## Symfony

84. Qu’est-ce que Symfony ?

    > Symfony est un framework PHP

85. Sur quel langage de programmation et design pattern repose Symfony ?

    > Langage PHP
    > design pattern MVC

86. Quelle est la dernière version en date de Symfony ?

    > Stable : 7.2

87. Qu’est-ce qu’un bundle ?

    > Un **_bundle_** est une sorte de plugin, il permet d'importer des fonctionnalités

88. Quel est le moteur de template utilisé par défaut dans Symfony ?

    > Twig

89. Qu’est-ce qu’un ORM ? Quel est son utilité et comment s’appelle-t-il au sein de Symfony ?

    > **Object Relational Mapping**, gère l'interaction entre la base de données et les objets utilisés par l'application
    > Au sein de Symfony, l'ORM est **Doctrine**

90. Qu’est-ce que l’injection de dépendances ? Quel est l’outil utilisé dans ce contexte et quel fichier contient l’intégralité des dépendances du projet ?

    > L'injection de dépendance permet de gérer la dépendences entre les objets

    ```php
    use Symfony\Component\DependencyInjection\ContainerBuilder;
    ```

    > L'outil utilisé est le **Service Container**, et l'intégralité des dépendances est dans le fichier services.yaml

91. Que permet le bundle Maker au sein de Symfony ?

    > Le bundle Maker permet de créer des fichiers via la commande
    > symfony console make:entity

92. Quel est le langage de requêtage exploité au sein d’un projet Symfony ?

    > DQL

93. Quel est le composant qui garantit l’authentification et l’autorisation des utilisateurs ?

    > security (security.yaml)

## Sécurité

94. Qu’est-ce que l’injection SQL ? Comment s’en prémunir ?

    > L'injection SQL est le fait pour un utilisateur malveillant d'accéder à une base de donnée et de la récupérer ou la modifier
    > Il est possible de s'en prévenir en préparant ces requêtes SQL avec des paramètres puis de les executer
    > **Requête paramétrée**

95. Qu’est-ce que la faille XSS ? Comment s’en prémunir ?

    > Cross Site Scripting, injection de contenu dans une page.
    > Peut rediriger, voler des informations (cookies par exemple), effectuer des actions, empecher la lecture de la page
    > On peut s'en prémunir en filtrant les contenus saisis par les utilisateurs

96. Qu’est-ce que la faille CSRF ? Comment s’en prémunir ?

    > Cross Site Request Forgery
    > Envoie de requêtes HTTP à l'insu de l'utilisateur (Qui a des droits particulier sur son application, admin)

    > On peut s'en prémunir avec des token CSRF à implémenter dans les formulaires
    > Une vérification est faite sur la correspondance du token reçu et envoyé

97. Définir l’attaque par force brute et l’attaque par dictionnaire

    > L'attaque par force brute consiste à chercher un mot de passe en essayant toutes les combinaisons possible
    > L'attaque par dictionnaire consiste à utiliser une librairie des mots de passe les plus courants

98. Existe-t-il d’autres failles de sécurité ? Citer celles-ci et expliquer simplement leur comportement

    > Déni de service distribué (DDoS), surcharge de trafic d'un site, qui le fait tomber en panne
    > Failles liées aux plugins et frameworks

99. A quoi servent l’authentification et l’autorisation dans un contexte d’application web ?

    > L'authentification permet de s'assurer que l'utilisateur est bien lui même (via identifiant et mot de passe)
    > Il est possible de bloquer certaines fonctionnalités d'une application web, empechant des actions à un 'guest' par exemple
    > Ou en ne permettant certaines actions qu'aux 'admins', on parle alors d'authorisation

100.    Définir la notion de hachage d’un mot de passe et citer des algorithmes de hachage

        > Le hachage transforme un mot de passe en une chaine de caractères plus complexe, afin de ne pas stocker "en clair" le mdp des utilisateurs.
        > Algorithme de hachage faible : md5 // sha256
        > Algorithme de hachage fort : bcrypt (defaut actuellement sur password_hash) // argon2i

101.    Qu’est-ce qu’une politique de mots de passe forts ?


    > Obligé l'utilisateur à créer un mot de passe complexe, voir recommandation CNIL

102. Qu’est-ce que l’hameçonnage ?


    > Récupérer des informations sensibles (d'authentification par exemple) via divers moyen (se faire passer pour un conseiller par exemple)

103. Définir la « validation des entrées »


    > Valide les données entrées par l'utilisateur lors de son login, en les comparant avec les infos stockées en BDD (et en verifiant le hash du mdp)

## RGPD

104. Qu’est-ce que le RGPD ?
105. Quel est son objectif principal ?
106. Quelle est la date d’entrée en vigueur du RGPD ?
107. Quelles sont les sanctions possibles en cas de non-respect du RGPD ?
108. En France, quel est l’autorité administrative qui s’occupe de faire appliquer le RGPD ?
109. Quel est le consentement valide selon le RPGD ?
110. Qu’est-ce qu’une politique de confidentialité ?
111. Quelle est la durée de conservation maximale des données personnelles selon le RGPD ?
112. Quels sont les droits des utilisateurs selon le RGPD ?
113. Qu’est-ce que le principe de minimisation des données selon le RGPD ?

## SEO

114. Qu’est-ce que le SEO ?
115. Quel est l’objectif principal du SEO ?
116. Existe-t-il plusieurs types de référencement ? Lesquels ?
117. Qu’est-ce que la densité de mots-clés en SEO ?
118. Qu’est-ce qu’une balise « alt » ?
119. Qu’est-ce que la balise « meta description » ?
120. Qu’est-ce que le « nofollow » en SEO ?
121. Quelle est l'importance du contenu de qualité pour le référencement d'un site web ?
122. Pourquoi est-il important d'utiliser des balises de titre (h1, h2, h3, etc.) de manière structurée ?
123. Quelle est la recommandation pour les URL d'un site web bien référencé ?
124. Qu'est-ce que le maillage interne et pourquoi est-il important pour le référencement ?
125. Qu'est-ce que l'optimisation des images pour le référencement ?
126. Qu'est-ce qu'un plan de site (sitemap) et pourquoi est-il important pour le référencement ?

## Gestion de projets - DevOps

127. Qu’est-ce que la gestion de projet ?
128. Qu’est-ce qu’une méthode Agile de gestion de projet ?
129. Expliquer la méthode MoSCoW en quelques lignes et citer ses avantages
130. A quoi sert la méthodologie MVP ? Citer les caractéristiques clés
131. Qu’est-ce que la planification itérative ?
132. Citer 3 méthodes Agiles dans le cadre d’un projet informatique
133. Qu’est-ce qu’une réunion de revue de projet ?
134. Qu’est-ce qu’un livrable dans un projet ?
135. Quels sont les 3 piliers SCRUM ? Définir chacun d’entre eux
136. Qu’est-ce que le DevOps et quel est son objectif principal ?
137. Qu’est-ce que l’intégration continue ?
138. Qu’est-ce que Docker ? Et en quoi est-il utile dans le cadre du DevOps ?
139. Qu’est-ce qu’un test unitaire ?
140. Quelle est l'unité de code testée lors d'un test unitaire ?
141. Quelles sont les caractéristiques d'un bon test unitaire ?
142. Qu'est-ce qu'une assertion dans un test unitaire ?

## English

1. What does JavaScript enable you to do on a website ?
   a. Add interactive behavior and dynamic content
   b. Define the layout and design of web pages
   c. Handle server-side operations
2. Which programming language is primarily used for server-side web development ?
   a. PHP
   b. JavaScript
   c. HTML
3. What is the purpose of a web browser ?
   a. To render and display web pages
   b. To execute serve-side code
   c. To manage databases
4. What is the difference between GET and POST methods in HTTP ?
   a. GET retrieves data from a server, while POST submits data to a server
   b. GET submits data to a server, while POST retrieves data from a server
   c. GET and POST methods are interchangeable
5. What is the purpose of version control systems (e.g., Git) in web development ?
   a. To track changes and manage collaborative development
   b. To optimize website loading speed
   c. To handle server-side scripting
6. What is the purpose of a framework in web development ?
   a. To provide a structured environment for building web applications
   b. To handle network protocols and data transfer
   c. To create visual designs and layouts for websites
7. What does NoSQL stand for ?
   a. Not Only SQL
   b. Non-Structured Query Language
   c. New Object-Oriented Language
8. Which of the following is a characteristic of NoSQL databases ?
   a. Strict schema enforcement
   b. Support for complex transactions
   c. Scalability and flexible data models
