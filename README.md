# Yasnad — Simulateur de montre connectée

Un simulateur de montre connectée personnalisable en Java avec interface graphique temps réel.

![Java](https://img.shields.io/badge/Java-17+-orange?logo=java) ![License](https://img.shields.io/badge/license-MIT-blue)

---

## Fonctionnalités

- **Affichage analogique & numérique** — aiguilles avec index ou texte HH:MM
- **Widgets modulaires** — secondes (trotteuse / mini-cadran / numérique), date, rythme cardiaque, batterie
- **Personnalisation complète** — forme du boîtier (rond, carré, arrondi), fond (uniforme / dégradé / image), couleurs
- **Simulation temporelle** — définir une heure de départ personnalisée
- **Config persistante** — sauvegarde et rechargement de chaque configuration (`.montre`)

---

## Installation & lancement

**Prérequis :** JDK 17+

```bash
# Cloner le projet
git clone https://github.com/ton-pseudo/yasnad.git
cd yasnad

# Compiler
mkdir -p bin
find src -name "*.java" | xargs javac -d bin -sourcepath src

# Lancer
java -cp bin montre.Main
```

---

## Structure du projet
src/montre/
├── Main.java
├── modele/          # Logique métier — Montre, ElementMontre, Boitier, FondCadran…
├── vue/             # Interface Swing — FenetreMontre, PanneauMontre, PanneauConfig
└── serialisation/   # Sauvegarde/chargement — GestionnaireMontre

---

## Technologies

- **Java 17** — langage principal
- **Swing** — interface graphique
- **Sérialisation Java** — persistance de la configuration

---

## Auteures

**Nada Cherine Chetloul** & **Yasmine Hadji** — L2 Informatique, Université de Picardie Jules Verne
