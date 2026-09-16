# 3. Transaction et pipeline d’exécution

Le pipeline commence par la validation de la transaction : type, nonce, limites de gas, solde, signature et règles du hardfork. Une transaction de création et un appel vers un contrat suivent ensuite des chemins différents.

L’interpréteur lit les opcodes, maintient la pile, la mémoire, le compteur de programme et le gas restant. Les appels créent des cadres imbriqués qui possèdent leur propre contexte tout en partageant certaines ressources.

Le handler coordonne les transitions entre validation, exécution, remboursement éventuel et construction du résultat. Les sorties distinguent le retour normal, le revert et l’arrêt par erreur.

ExecuteEvm propose aussi l’exécution de plusieurs transactions, avec une finalisation qui peut regrouper les écritures.

Suite : [Journal, commit et rollback](04-journal-commit-rollback.md).
