# 5. FRI et politique d’acceptation

Le [vérificateur](../../verifier/src/lib.rs) reconstruit les défis FRI, contrôle le nonce de grinding et tire les positions de requête.
Il trie et déduplique ces positions avant de lire les ouvertures de trace et de contraintes.
Les engagements authentifient les valeurs ouvertes ; le compositeur DEEP prépare les évaluations utilisées par la vérification FRI.
[FRI](../../fri/src/lib.rs) fournit le contrôle probabiliste de bas degré, pas une vérification exhaustive de chaque ligne de trace.
Au début de `verify`, `AcceptableOptions` impose aussi la politique choisie par l’appelant.
Les variantes sont `MinConjecturedSecurity`, `MinProvenSecurity` et `OptionSet`.
Accepter une preuve syntaxiquement lisible ne suffit donc pas : ses paramètres doivent satisfaire cette politique.
Les niveaux conjecturés et prouvés correspondent à des critères distincts ; ne pas les présenter comme synonymes.
L’application doit choisir explicitement ses paramètres et conserver la même définition des entrées publiques.

Suite : [Limites, tests et place dans un rollup](06-limites-rollups.md).
