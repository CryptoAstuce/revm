# 5. Précompilés et variantes EVM

Les précompilés sont des adresses spéciales dont le calcul est fourni par l’environnement plutôt que par du bytecode ordinaire. revm regroupe ces fonctions dans un PrecompileProvider et calcule leur coût ainsi que leur sortie.

Les précompilés cryptographiques couvrent des opérations comme les signatures, le hachage, l’exponentiation modulaire et les courbes utilisées par les preuves. Leur disponibilité dépend du hardfork et de la variante de chaîne.

Le provider peut être remplacé pour ajouter une règle spécifique ou supporter une chaîne compatible EVM. Le moteur conserve le même pipeline, mais le contexte et les instructions peuvent changer.

Cette extensibilité explique l’usage de revm dans des environnements Ethereum et dans des rollups qui ajoutent leurs propres transactions système ou coûts.

Suite : [Inspection, intégration et limites](06-inspection-integration-limites.md).
