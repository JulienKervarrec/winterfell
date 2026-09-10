# 4. Engagements et défis du vérificateur

Dans [verify](../../verifier/src/lib.rs), la graine initiale du générateur aléatoire combine le contexte de la preuve et les entrées publiques.
Le vérificateur reconstruit ainsi des défis à partir des données du protocole plutôt que de faire confiance à des défis choisis librement par le prouveur.
Les engagements de trace alimentent ce transcript ; les segments auxiliaires peuvent demander des défis supplémentaires.
Après les coefficients de combinaison des contraintes, l’engagement correspondant alimente à son tour le transcript.
Le point hors domaine sert à comparer l’évaluation des contraintes AIR avec celle du polynôme de composition.
Une incohérence produit un rejet avant la dernière vérification FRI.
Les évaluations hors domaine sont ensuite intégrées au transcript avant les étapes suivantes.
L’ordre des engagements et des défis fait partie du protocole : ce n’est pas une simple liste de hachages interchangeable.
Cette lecture décrit le chemin du vérificateur ; elle n’est pas une démonstration de sécurité du protocole.

Suite : [FRI et politique d’acceptation](05-fri-politique.md).
