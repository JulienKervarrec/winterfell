# 6. Limites, tests et place dans un rollup

Ce parcours est documentaire : aucune installation, compilation ou exécution de tests n’a été réalisée pour ces chapitres.
Les [tests Fibonacci](../../examples/src/fibonacci/fib2/tests.rs) comprennent des cas de vérification, d’extension de corps et d’échec ; leur présence ne signifie pas qu’ils ont été exécutés ici.
Le [README amont](../../README.md) présente Winterfell comme un logiciel de recherche non audité et non prêt pour la production.
Il signale également l’absence de confidentialité parfaite ; ce parcours ne transforme pas cette limite en garantie ZK.
Une preuve de Fibonacci n’est pas un zk-rollup.
Pour un rollup, il reste notamment à définir la transition d’état, les transactions autorisées, les engagements d’état et le lien avec le contrat de règlement.
La disponibilité des données, les dépôts et retraits, ainsi que les mécanismes de mise à jour restent des responsabilités de l’application.
Le fork ne modifie ni le prouveur ni le vérificateur et ne revendique aucun audit.
Pour vérifier ou prolonger la lecture, partir des sources et des tests liés ci-dessus, puis suivre les instructions amont dans un environnement adapté.

Retour au [sommaire](README.md).
