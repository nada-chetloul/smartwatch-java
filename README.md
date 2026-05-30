# Simulateur de montre connectée

Yasnad est une application Java qui simule une montre connectée avec une interface graphique interactive. On peut personnaliser l'affichage en temps réel : changer le style du cadran, activer des widgets, modifier les couleurs, et même simuler une heure personnalisée. La configuration peut être sauvegardée et rechargée à tout moment.

![Java](https://img.shields.io/badge/Java-17+-orange?logo=java) ![Swing](https://img.shields.io/badge/UI-Swing-blueviolet) ![License](https://img.shields.io/badge/license-MIT-blue)

---

## Aperçu

![Affichage analogique](images/analog.png)

![Affichage numérique](images/digital.png)

![Tous les widgets actifs](images/full.png)

---

## Fonctionnalités

### Affichage de l'heure
- **Mode analogique** — aiguilles des heures et minutes, chiffres 1–12, graduations minutières
- **Mode numérique** — heure affichée en grand au centre (HH:MM) en police Courier New

### Panneau de personnalisation
Un panneau latéral scrollable permet de tout configurer en temps réel sans relancer l'application :
- **Boîtier** — 3 formes disponibles (rond, carré, arrondi), couleur et épaisseur du bord personnalisables
- **Fond du cadran** — uniforme, dégradé deux couleurs, ou image personnalisée en arrière-plan
- **Affichage heure** — basculer entre analogique et numérique, afficher ou masquer les chiffres
- **Éléments optionnels** — activer/désactiver indépendamment chaque widget
- **Simulation** — définir une heure de départ (heures, minutes, secondes) qui avance en temps réel

### Widgets optionnels
- **Secondes** — trotteuse sur le cadran, mini-cadran secondaire, ou compteur numérique
- **Date** — 4 formats disponibles (dd/MM, dd/MM/yy, EEE dd, EEE dd MMM) en français
- **Batterie** — lecture du niveau réel sur Linux, indicateur vert/rouge selon le niveau
- **Rythme cardiaque** — simulation BPM avec icône cœur

### Sauvegarde
- Sauvegarde et rechargement de toute la configuration dans un fichier `.montre`
- Accessible via le menu **Fichier** avec raccourcis clavier (Ctrl+S, Ctrl+O)

---

## Installation & lancement

**Prérequis :** JDK 17+

    # Cloner le projet
    git clone https://github.com/nada-chetloul/smartwatch-java.git
    cd smartwatch-java

    # Compiler
    mkdir -p bin
    find src -name "*.java" | xargs javac -d bin -sourcepath src

    # Lancer
    java -cp bin montre.Main

---

## Structure du projet

    src/
    └── montre/
        ├── modele/
        │   ├── Montre.java
        │   ├── ElementMontre.java
        │   ├── Boitier.java
        │   ├── FondCadran.java
        │   ├── AffichageHeure.java
        │   ├── AffichageAnalogique.java
        │   ├── AffichageNumerique.java
        │   ├── ElementDate.java
        │   ├── ElementSecondes.java
        │   ├── ElementBatterie.java
        │   └── ElementRythmeCardiaque.java
        │
        ├── vue/
        │   ├── FenetreMontre.java
        │   ├── PanneauMontre.java
        │   └── PanneauConfig.java
        │
        └── serialisation/
            └── GestionnaireMontre.java

---

## Technologies

- **Java 17** — langage principal
- **Swing** — interface graphique (JFrame, JPanel, JComboBox, JColorChooser…)
- **Sérialisation Java** — sauvegarde de la configuration via ObjectOutputStream

---

## Auteure

**Nada Cherine Chetloul** — L2 Informatique, Université de Picardie Jules Verne
