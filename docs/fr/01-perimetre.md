# 1. Ce que prouve Winterfell

Winterfell fournit un prouveur et un vérificateur STARK pour décrire et vérifier des calculs.
Le [README](../../README.md) distingue ce cadre générique d’une application prête à déployer.
Une preuve atteste la cohérence d’un calcul avec des contraintes ; elle ne décide pas si ces contraintes expriment le bon besoin métier.
L’absence de cérémonie de confiance ne signifie pas absence d’hypothèses cryptographiques.
Le README indique aussi que la confidentialité parfaite n’est pas actuellement fournie : « STARK » ne suffit donc pas à promettre le secret des données.
Ce parcours suit l’exemple Fibonacci à deux colonnes, puis le vérificateur.
Les composants principaux sont [air](../../air), [prover](../../prover), [verifier](../../verifier) et [fri](../../fri).
La lecture porte sur la révision amont `2f78ee9bf667a561bdfcdfa68668d0f9b18b8315` ; les liens relatifs suivent ce fork.

Suite : [Deux valeurs par ligne](02-trace-fibonacci.md).
