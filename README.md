
# Projet : Protocole AuctionP2P

## Statut du projet
Projet en cours de réalisation.  
La divulgation complète du projet est interdite avant la fin de l'examen.

## I) Présentation du protocole

**AuctionP2P** est un protocole d’enchères entre pairs (P2P).  
Chaque pair peut :
- Débuter une vente aux enchères avec un prix initial.
- Enchérir en proposant un prix supérieur au prix en cours.
- Participer librement tant que l’enchère est active.

La vente se termine lorsqu'aucune nouvelle proposition n'est reçue pendant un certain temps.

**Remarque** : Ce projet ne doit pas être distribué, utilisé ou modifié sans autorisation préalable. L'accès au code source et à la documentation est limité à des fins éducatives ou de démonstration dans un cadre spécifique.

## II) Paramètres de fonctionnement

Le protocole AuctionP2P nécessite plusieurs paramètres pour fonctionner correctement :

1. **Adresse liaison** :  
   Adresse IPv6 de multidiffusion avec son port, utilisée pour rejoindre le système d’enchères entre pairs.

2. **Adresse personnelle (adressePerso)** :  
   Adresse IPv6 et port d’écoute pour la communication en mode TCP et UDP pour chaque pair.

3. **Adresse des enchères** :  
   Adresse IPv6 et port de multidiffusion pour la communication entre tous les pairs.

4. **Identifiant unique** :  
   Chaque pair doit posséder un identifiant unique dans le système d’enchères.

5. **Clé publique/privée (ED25519)** :  
   Chaque pair doit disposer d'une paire de clés au format ED25519 pour assurer la sécurité des transactions.

## III) Fonctionnement du consensus

Le protocole étant pair-à-pair, un consensus est nécessaire pour valider les transactions. Si deux pairs envoient simultanément la même proposition de prix, les autres pairs recevront les propositions dans un ordre pouvant varier d’un pair à l’autre. Ce mécanisme de gestion des propositions garantit une validation sécurisée et fiable des enchères.

## IV) Conclusion

Le protocole AuctionP2P permet des enchères décentralisées et sécurisées, où chaque pair peut participer librement et où un consensus est nécessaire pour valider chaque transaction. L’utilisation des clés ED25519 garantit la sécurité des transactions.
