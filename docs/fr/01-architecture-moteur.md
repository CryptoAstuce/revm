# 1. Architecture du moteur

revm est un moteur d’exécution EVM écrit en Rust. Le dépôt le présente à la fois comme un exécuteur capable de rejouer des transactions et comme un framework pour adapter différentes variantes de l’EVM, notamment Optimism.

L’architecture est découpée en crates : bytecode, interpreter, context, database, handler et precompile. Cette séparation permet de remplacer une partie sans réécrire toute la machine.

L’objet EVM orchestre le contexte, la transaction, l’accès à la base et le handler. Le handler assemble les étapes de validation, d’exécution et de finalisation.

Cette modularité est utile pour les nœuds, les simulateurs, les outils de test et les environnements qui veulent contrôler précisément les règles d’exécution.

Suite : [Environnement et état](02-environnement-etat.md).
