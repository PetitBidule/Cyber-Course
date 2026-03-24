Trafic en clair autorisé : android:usesCleartextTraffic=true.
Cela veut dire que l’application peut accepter des communications non chiffrées, ce qui expose à l’interception ou à la modification du trafic réseau. C’est l’un des points les plus sensibles du rapport.
Compatibilité avec des versions Android trop anciennes : le minSdk=19 permet l’installation sur Android 4.4.x, une version connue pour comporter de nombreuses failles non corrigées.

Cryptographie faible ou risquée :
usage de SHA-1 dans la signature, algorithme ancien avec risques de collision ;
usage de MD5 dans le code, également considéré faible ;
usage du mode AES-CBC avec PKCS5/PKCS7, signalé comme exposé à des attaques de type padding oracle si mal implémenté.

Composants Android exposés : plusieurs receivers, services et un content provider sont exportés ou insuffisamment protégés. Cela peut permettre à d’autres applications sur le téléphone d’interagir avec eux de façon non souhaitée.

Stockage peu sûr :
l’application peut lire/écrire sur le stockage externe ;
des fichiers temporaires peuvent être créés ;
MobSF indique aussi la présence potentielle de données sensibles en dur dans certains fichiers.vb 

Qualité de code / sécurité applicative :
présence de logs pouvant contenir des informations sensibles ;
exécution de requêtes SQL brutes, avec un risque potentiel de SQL injection si une entrée non fiable y arrive ;
usage d’un générateur aléatoire insuffisamment sûr dans certaines parties du code.