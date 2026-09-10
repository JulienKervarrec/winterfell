# 2. Deux valeurs par ligne

Dans [build_trace](../../examples/src/fibonacci/fib2/prover.rs), deux colonnes contiennent des termes consécutifs de Fibonacci.
L’état initial est `(1, 1)`.
Chaque transition exécute d’abord `state[0] += state[1]`, puis `state[1] += state[0]` avec la première valeur déjà mise à jour.
Les premières lignes sont donc `(1,1) → (2,3) → (5,8)`, et non deux additions indépendantes sur l’ancien état.
Pour une longueur de séquence `n`, le constructeur réserve `n / 2` lignes et exige que `n` soit une puissance de deux.
Cette condition ne remplace pas les autres préconditions de taille de la bibliothèque.
La trace représente le calcul complet ; ce n’est pas ce tableau entier que l’application transmet comme résultat public.
`get_pub_inputs` expose la valeur de la seconde colonne à la dernière ligne.
Changer cette valeur publique change l’énoncé que le vérificateur doit accepter.

Suite : [Relier transitions et résultat](03-contraintes-air.md).
