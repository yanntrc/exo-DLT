# 1 - Un arbre de merkle nécessite une paire de hashes pour produire un nouveau hash parent. Il faut donc absolument que le nombre de transactions qui produiront le Merkle root soit pair. Comment est géré le cas ou le nombre de transactions dans le Block à valider est impair pour générer un Merlke root ?

Si il y a un nombre de transaction impair dans le block, le dernier noeud est dupliqué et hashé avec lui-même.

# 2 - Dans le réseau bitcoin, Comment un nouveau noeud arrive t'il à retrouver ses pairs et ainsi rejoindre le réseau ? Expliquer le processus avec vos propres mots.

Le nouveau noeud se connecte au réseau via bitcoin core. Il est possible de configurer soit meme sa machine pour s'y connecter, avec un Raspberry Pi par exemple, mais il existe égaelement des solutions clé en main tel que nodl.

# 3 - Pouvez vous nommer au moins une personne qui a ou aurait pu influencer directement ou indirectement la création de Bitcoin par ses travaux (une personne qui n'a pas été nommée dans le cours)?

1992 : Dans un document de recherche intitulé « Pricing via pocessing or combatting junk mail » , Cynthia Dwork et Moni Naor introduisent l’idée de preuve de travail.

# 4 - Avec vos propres recherches et grâce aux compétences acquises en cours pouvez vous expliquer comment une Blockchain crée un lien entre ses différents Blocks?

La relation entre les deux blocs est effectuée gràce à une fonction, qui prend en parametre l'ancien bloc, et retourne une valeur numerique, qui sera mise dans le nouveau bloc.

# 5 - Quelle structure de données informatique peut représenter le mieux cette chaine de Block: https://en.wikipedia.org/wiki/List_of_data_structures ?

It is a hash tree

# 6 - Si je souhaite modifier une transaction de 10 bitcoin que j'ai effectué il y a 6 mois en une transaction de 1 Bitcoin, que dois je modifier dans la Blockchain et que dois je mettre en oeuvre pour que cette modification persiste ? Est ce possible selon vous ?

Il faudrait pour cela récuperer le bloc d'il y a six mois, réecrire la partie qui concerne cette transaction en remplacement 10 bitcoins par 1 bitcoin, puis trouver le hash correspondant pour ce bloc, puis pour tous les blocs suivants. Cela pose deux problèmes: en faisant cela, on crée une version alternative de la blockchain, qui est donc en competion avec celle qu'on tente d'alterer. Il faudra donc miner en parralèle du reste des mineurs. Il faudra donc continuer de miner si on vont tenter de faire valider cette transaction. Cela ammène au deuxième problème: il faudrait une puissance de calcul phénomènale pour rentrer en compétition avec le reste du réseau.
Ce n'est donc pas possible avec les technologies actuelles, sinon quelqu'un l'aurait probablement déjà fait.
