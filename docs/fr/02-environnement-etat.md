# 2. Environnement et état

Le contexte fournit les informations de bloc, de transaction et de configuration de l’EVM. Il contient notamment le numéro de bloc, le timestamp, le gas limit, le caller, la valeur transférée et l’adresse ciblée.

La base Database abstrait la lecture des comptes, du code, du stockage et des blocs. Une implémentation peut servir un état local, une base distante ou un état de fork.

Le cache évite les lectures répétées pendant une transaction. Il reste distinct de l’état durable : une lecture mise en cache n’est pas encore une écriture validée.

Les règles de hardfork déterminent les opcodes, les coûts de gas et les changements de protocole applicables au contexte choisi.

Suite : [Transaction et pipeline d’exécution](03-transaction-pipeline.md).
