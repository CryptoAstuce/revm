# 6. Inspection, intégration et limites

Un inspector observe les étapes de l’interpréteur sans devenir lui-même la source de vérité de l’état. Il peut produire des traces, mesurer les opcodes ou implémenter des outils de développement comme des cheatcodes.

L’intégrateur doit choisir avec soin la base, le hardfork, les précompilés, les règles de gas et la politique de commit. Deux configurations différentes peuvent donner des résultats différents à transaction identique.

La performance du moteur ne garantit pas la conformité d’un environnement mal configuré. revm fournit les briques d’exécution ; le nœud ou l’outil appelant reste responsable de l’acquisition de l’état et de la validation du contexte.

Périmètre : ce parcours traduit les crates d’exécution, handler, database, interpreter, bytecode et precompile présentes dans le dépôt. Aucune installation, compilation ou exécution de test n’a été effectuée. Consulter les suites du dépôt pour une vérification concrète.

Retour : [sommaire du parcours](README.md).
