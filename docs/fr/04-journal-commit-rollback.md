# 4. Journal, commit et rollback

Pendant l’exécution, les mutations sont enregistrées dans un journal. Le moteur peut ainsi appliquer les changements à la fin d’un parcours réussi ou les annuler lorsqu’un appel échoue.

Cette distinction protège l’état contre les effets partiels d’un revert. Un appel interne peut avoir écrit dans le stockage avant de revenir en erreur ; le journal permet de restaurer la vue cohérente attendue.

Les exécutions multiples peuvent partager un état de travail, puis être finalisées ensemble. Les traits ExecuteEvm et ExecuteCommitEvm séparent précisément l’exécution de la décision de commit.

La finalisation produit aussi les changements d’état utiles à l’intégrateur : comptes touchés, stockage modifié, code déployé et remboursements.

Suite : [Précompilés et variantes EVM](05-precompiles-variantes.md).
