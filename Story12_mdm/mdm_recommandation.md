# MDM Recommandation


## 1. Solutions comparées

- **Microsoft Intune**
- **VMware Workspace ONE UEM**

## 2. Critères de comparaison

Les critères retenus sont :
- couverture fonctionnelle MDM / UEM ;
- compatibilité Android Enterprise ;
- capacité à contrôler la distribution applicative ;
- intégration avec l’écosystème IAM et sécurité ;
- simplicité d’administration ;
- capacité de reporting et conformité ;
- coût et cohérence avec l’existant.

## 3. Tableau comparatif

| Critère | Microsoft Intune | Workspace ONE UEM |
|---|---|---|
| Positionnement | MDM/UEM fortement intégré à l’écosystème Microsoft | UEM complet, historiquement très fort sur la gestion de flotte |
| Gestion Android Enterprise | Oui, couverture complète des usages courants | Oui, couverture complète et mature |
| Store d’entreprise / catalogue applicatif | Oui, avec publication et contrôle des applications approuvées | Oui, avec catalogue d’entreprise et distribution centralisée |
| Contrôle de l’installation des APK | Bon niveau de contrôle via politiques de conformité et restrictions | Bon niveau de contrôle, y compris pour environnements fortement administrés |
| Intégration identité / accès | Excellente avec Entra ID, Conditional Access, Microsoft 365 | Bonne, mais moins native si l’environnement est majoritairement Microsoft |
| Protection des données | Forte intégration avec les politiques applicatives Microsoft | Bonne couverture, plus dépendante du paramétrage global |
| Administration | Souvent plus simple si l’entreprise utilise déjà Microsoft 365 | Très riche, mais parfois plus complexe à administrer |
| Expérience sur parc hétérogène | Bonne | Très bonne |
| Terminaux spécialisés / usages terrain | Correct | Souvent meilleur |
| Reporting / conformité | Bon niveau, intégré à la gouvernance Microsoft | Bon niveau, avec capacités avancées |
| Coût global | Souvent avantageux si licences Microsoft déjà présentes | Variable, souvent plus coûteux selon le périmètre |
| Pertinence pour un SI Microsoft | Très forte | Moyenne à forte selon l’existant |

## 4. Analyse

### 4.1 Microsoft Intune

**Points forts :**
- très bonne intégration avec Microsoft 365, Entra ID et les mécanismes d’accès conditionnel ;
- cohérence forte entre gestion des terminaux, gestion des identités et sécurité des accès ;
- administration souvent plus simple dans un environnement déjà standardisé Microsoft ;
- bon alignement avec une politique Android imposant l’installation des applications uniquement depuis un store d’entreprise.

**Points de vigilance :**
- moins différenciant si l’entreprise a un parc très hétérogène ou des besoins avancés sur terminaux spécialisés ;
- certaines fonctions avancées peuvent dépendre de la maturité de l’écosystème Microsoft déjà en place.

### 4.2 Workspace ONE UEM

**Points forts :**
- solution UEM mature et robuste ;
- très bonne gestion des environnements hétérogènes ;
- adaptée aux flottes complexes, aux usages terrain et à certains besoins avancés de gestion de terminaux ;
- bon niveau de contrôle sur la distribution applicative et la posture terminal.

**Points de vigilance :**
- intégration parfois moins naturelle dans un SI centré sur Microsoft ;
- complexité d’administration potentiellement plus élevée ;
- coût global parfois moins favorable selon le contexte de licences.

## 5. Recommandation

### Recommandation proposée : **Microsoft Intune**

Microsoft Intune est recommandé comme solution MDM cible **dans le cas général d’une organisation déjà équipée ou en cours de standardisation sur Microsoft 365**.

Cette recommandation repose sur les éléments suivants :
- intégration native avec les services d’identité et de sécurité Microsoft ;
- capacité à appliquer des politiques homogènes sur les terminaux Android ;
- aptitude à encadrer la distribution applicative via un canal d’entreprise maîtrisé ;
- coût et effort d’intégration potentiellement mieux maîtrisés si les briques Microsoft sont déjà déployées ;
- meilleure cohérence d’architecture pour une approche sécurité centrée sur identité, conformité terminal et contrôle d’accès.