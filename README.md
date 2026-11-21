# Java Projects

Two Java exercises: a playable terminal game and a small geometry library.

## Allumettes matchstick game

Start with 13 matchsticks. On each turn, take 1, 2, or 3 of the remaining matchsticks. The player who takes the last one loses.

### Play against the computer

You’ll need a JDK with `javac` and `java` on your PATH. From the repository root, run these commands in a terminal on macOS or Linux. The build command compiles the game sources and skips the test files.

```sh
cd "Matchstick Project"
mkdir -p out
find . -type f -name '*.java' ! -name '*Test.java' -exec javac -d out {} +
java -cp out allumettes.Jouer You@humain Computer@rapide
```

The game prompts you in French. Type a number and press Enter. If you take two matchsticks on your first turn, the computer takes three, leaving eight for your next turn.

```text
Allumettes restantes : 13
You, combien d'allumettes ? 2
You prend 2 allumettes.

Allumettes restantes : 11
Computer prend 3 allumettes.

Allumettes restantes : 8
```

Each player is configured as `name@strategy`. Replace `Computer@rapide` with `Friend@humain` for a two-player game, or try `Computer@expert` for a different computer strategy.

[Browse the game source](Matchstick%20Project) · [Command-line entry point](Matchstick%20Project/Jouer.java)

## Circle geometry

The [circle exercise](Cercle%20Project) models a circle with a center and radius. It supports translation, point containment, and calculations for diameter, perimeter, and area. [`Cercle.java`](Cercle%20Project/Cercle.java) contains the implementation.
