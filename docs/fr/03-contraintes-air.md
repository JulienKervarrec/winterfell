# 3. Relier transitions et résultat

L’[AIR Fibonacci](../../examples/src/fibonacci/fib2/air.rs) encode deux contraintes de transition de degré un.
Pour une ligne courante `(a,b)` et la suivante `(a′,b′)`, il exige `a′ = a + b` et `b′ = b + a′`.
Le prouveur construit une trace ; l’AIR est la définition indépendante des relations auxquelles cette trace doit satisfaire.
Trois assertions de frontière fixent la première colonne à 1 au début, la seconde à 1 au début et la seconde au résultat public à la fin.
Sans l’état initial, une autre suite pourrait satisfaire les mêmes transitions.
Sans la frontière finale, les transitions ne lieraient pas le calcul au résultat annoncé.
`AirContext::new` reçoit les degrés et le nombre d’assertions ; ces métadonnées participent à la construction du protocole.
Une contrainte oubliée n’est pas ajoutée magiquement par le système de preuve.
Pour adapter cet exemple, décrire d’abord l’énoncé et ses frontières, puis seulement le constructeur de trace.

Suite : [Engagements et défis du vérificateur](04-transcript.md).
