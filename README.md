# Travail dirigé préparatoire

Ce travail dirigé prépare l'étudiant en vue du travail écrit du jeudi 18 janvier 2024.

## Consignes

- Vous pouvez utiliser les notes de cours, internet et vos notes personnelles.
- A la fin des 4 périodes de travail vous devez avoir terminé les 6 problèmes.
- Commit et push à la fin de chaque problème.

## Objectifs

À la fin de ce travail dirigé, l'étudiant sera en mesure de :

- Revoir les concepts de base de la programmation orientée objet
- Valider l'aquisition des concepts évoqués dans la fiche d'unité

## Problèmes

### Problème 1 : C++

Écrire un programme `pb1.cpp` qui met en oeuvre les éléments suivants :

- Interface abstraite
- Classe réalisaant l'interface abstraite
- Pointeur vers une instance de la classe réalisée
- Attributs et méthodes publiques et privées
- Constructeur par défaut
- Constructeur avec paramètres

Le programme dispose d'un `main` qui instancie un objet de la classe et qui appelle les méthodes de l'objet.

1. Démontrer le fonctionnement du programme.
2. Démontrer que les bonnes méthodes sont appelées
3. Démontrer l'existance de vtables (utilisez `objdump -d` ou le site godbolt).

### Problème 2 : STL

Écrire un programme `pb2.cpp` qui met en oeuvre les éléments suivants :

- Vecteur de pointeurs vers une `Shape`.
- Réalisation d'une classe `Square`, `Triangle` et d'une classe `Circle` qui héritent de `Shape`.
- Chaque `Shape` dispose également d'une couleur selon une `enum class` de quelques coloris.
- Chaque `Shape` dispose d'une position et d'une aire.
- Une méthode `draw` permet d'afficher avec SFML la forme à l'écran, à la position donnée.
- Une méthode `edge` retourne la taille d'une arête de la forme.

Dans le main:

1. Insérer avec `emplace_back` aléatoirement 20 formes différentes (cercles, carrés, triangles).
2. Afficher ces formes à l'écran.
3. Faire tourner les formes sur elles-mêmes (avec `rotate`) avec la molette de la souris.

### Problème 3 : Templates

Écrire un programme `pb3.cpp` qui met en oeuvre les éléments suivants :

- Implémenter une template `PriorityQueue` qui contient un `std::priority_queue`.
- Ce container doit permettre d'insérer des éléments de type `T` avec une priorité.
- Une méthode `tail(int n, std::function<void(T)> f)` permet d'itérer sur les `n` éléments de plus haute priorité et d'appeler la fonction `f` sur chacun d'eux.

Dans le main:

1. Insérer 1000 éléments, par exemple un point X,Y aléatoires entre 0 et 1000 avec une priorité aléatoire entre 0 et 1000.
2. Afficher les 10 éléments de plus haute priorité sur la sortie standard.

### Problème 4 : Allocation dynamique

Écrire un programme `pb4.cpp` qui met en oeuvre les éléments suivants :

- Smart Pointers (std::unique_ptr, std::shared_ptr)
- Allocation dynamique avec `new` et `delete`
- Concept RAII

Objectifs:

1. Montrer l'intérêt d'un smart-pointer par rapport à un pointeur classique.
2. Expliquer comment un smart-pointer permet d'être RAII.

### Problème 5 : Exceptions

Écrire un programme `pb5.cpp` qui met en oeuvre les éléments suivants :

- Exceptions
- Gestion des exceptions
- `try` et `catch`
- `throw`

Objectifs:

1. Créer une classe `File` qui permet de lire un fichier texte.
2. Créer plusieurs exceptions qui peuvent être levées par la classe `File` (par exemple `FileNotFound`, `FileNotReadable`, `FileNotWritable`). Chaque exception contient un message d'erreur, et le nom du fichier concerné.

Montrer dans le main que les exceptions sont bien levées et gérées.

### Problème 6 : Problème du diamant

Montrer dans le fichier `pb6.cpp` que le problème du diamant est bien résolu par le compilateur C++ en utilisant les mots clés adaptés. Le programme peut être compilé avec une définition `#define DIAMOND` ou non (appelé depuis le compilateur `g++ -DDIAMOND`).

1. Si le programme est compilé avec `DIAMOND`, montrer que le problème du diamant est bien résolu.
2. Si le programme est compilé sans `DIAMOND`, montrer que le problème du diamant n'est pas résolu.
