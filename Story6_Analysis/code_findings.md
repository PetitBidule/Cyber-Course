## Analyse de code

### Exposition de FireBase

Présence de fichier Firebase dans l'apk et accès à l'URL de la bdd Firebase:

`<string name="firebase_database_url">https://application-client-nickel.firebaseio.com</string>`

### Données sensibles dans certains fichiers

Une des faiblesses les plus critiques dans une applications Android décompilé est la présence de données sensibles dans le code ou les ressoucres.
Des clés API, tokens, ou encore des URLS peuvent être récupéres en analysant l'APK
Par exemple dans le fichier `res/values/strings.xml` avec des clé api.

L'impact est qu'un attaquant peut extraire ces informations pour intéragir directement avec l'API

### Manque de protections contre le reverse engineering

L'impact, analyse de fichier avec des outils comme jadx et donc modifications de l'app

### Configuration réseau

Dans le fichier `AndroidManifest.xml`, nous avons la ligne suivante `android:usesCleartextTraffic="true">` ce qui autorise les communications HTTP non chiffrées, donc expose les données échangés à des attaques MITM
