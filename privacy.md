# Politique de confidentialité — Itadaki

**Dernière mise à jour :** 27/09/2026

Itadaki respecte ta vie privée. Cette politique explique quelles données sont traitées, pourquoi, par qui et combien de temps, ainsi que les droits dont tu disposes.

## 1) Responsable du traitement
**Éditeur :** Axel Legué (développeur indépendant)
**Contact :** itadaki.app@gmail.com
**Pays :** France

## 2) Principe : tes données restent sur ton appareil
Tes recettes, menus, listes de courses et préférences sont enregistrés **localement sur ton appareil**. L’éditeur n’y a pas accès.

L’application fonctionne **sans compte**. Une **connexion Google facultative** est proposée (voir section 3.2). Certaines fonctionnalités font appel à des services tiers, décrits ci-dessous.

## 3) Données traitées

### 3.1 Données que tu fournis
- **Contenu de recette** que tu saisis ou modifies (titre, ingrédients, étapes, photos, etc.) : stocké uniquement sur ton appareil.
- **Photos** prises ou choisies pour l’**import de recette par IA** : envoyées au service d’IA pour analyse (voir section 6).
- **Liens (URL) de recettes** et, pour les publications de réseaux sociaux (ex. Instagram, TikTok), **le texte de la publication** : envoyés au service d’IA lorsque l’import par lien le nécessite (voir section 6).
- **Identifiants WebDAV** (adresse du serveur, nom d’utilisateur, mot de passe) si tu configures cette sauvegarde : stockés sur ton appareil, le mot de passe étant chiffré.

### 3.2 Connexion Google (facultative)
Si tu choisis de te connecter avec Google, nous recevons via **Firebase Authentication** : un **identifiant unique**, ton **adresse e-mail** et ton **nom d’affichage**.

Ce compte sert uniquement à conserver tes **compteurs d’utilisation** (nombre d’imports IA et d’imports web utilisés) dans **Cloud Firestore**, pour qu’ils suivent ton compte d’un appareil à l’autre. **Tes recettes ne sont pas envoyées sur nos serveurs.**

### 3.3 Sauvegarde (facultative, à ton initiative)
Tu peux exporter ou sauvegarder tes données :
- **vers un fichier** à l’emplacement de ton choix ;
- **vers Google Drive** : la sauvegarde est placée dans un **dossier privé réservé à l’application** (autorisation `drive.appdata`) ; l’application n’a pas accès au reste de ton Drive ;
- **vers un serveur WebDAV** que tu choisis.

Ces sauvegardes sont transmises directement de ton appareil vers le service choisi ; l’éditeur n’y a pas accès. Leur conservation relève de ce service et de toi.

### 3.4 Données collectées automatiquement
- **Diagnostic (Firebase Crashlytics)** : rapports de plantage, trace technique, modèle d’appareil, version d’Android et de l’application.
- **Statistiques d’usage (Google Analytics for Firebase)** : identifiant d’instance de l’application, informations techniques et événements liés à l’offre premium (affichage de l’écran d’abonnement, début, réussite ou échec d’un achat, fonctionnalité premium bloquée), ainsi que les événements collectés automatiquement par le SDK (ex. première ouverture, durée de session).
- **Achats (Google Play Billing)** : statut de ton abonnement et informations de transaction, gérés par Google Play. L’éditeur ne reçoit **jamais** tes coordonnées bancaires.
- **Protection du service (Firebase App Check / Play Integrity)** : vérification que les requêtes proviennent bien de l’application authentique, afin d’éviter les abus des services d’IA.
- **Configuration à distance (Firebase Remote Config)** : récupération de paramètres techniques de l’application (ex. choix du modèle d’IA).

L’application **n’affiche pas de publicité** et ne vend pas tes données.

## 4) Finalités et bases légales (RGPD)

| Finalité | Données | Base légale |
|---|---|---|
| Fournir les fonctionnalités de l’app (recettes, menus, liste de courses) | Contenu saisi (local) | Exécution du contrat |
| Importer une recette par IA (photo ou lien) | Photos, URL, texte de publication | Exécution du contrat (fonctionnalité que tu déclenches) |
| Connexion Google et synchronisation des compteurs d’utilisation | Identifiant, e-mail, nom, compteurs | Exécution du contrat |
| Sauvegarde Google Drive / WebDAV | Tes données exportées, identifiants WebDAV | Exécution du contrat (à ta demande) |
| Gérer les abonnements | Statut d’abonnement, transactions | Exécution du contrat et obligations légales |
| Corriger les bugs et assurer la stabilité | Données de diagnostic | Intérêt légitime |
| Protéger le service contre les abus | Données d’intégrité de l’appareil et de l’app | Intérêt légitime |
| Mesurer l’usage et améliorer l’offre | Statistiques d’usage | Consentement lorsque requis, sinon intérêt légitime |

## 5) Destinataires et sous-traitants
Nous ne vendons ni ne louons tes données. Elles peuvent être traitées par :
- **Google Firebase** (Authentication, Cloud Firestore, Crashlytics, Analytics, App Check, Remote Config, Firebase AI Logic) ;
- **Google** (API Gemini, via Firebase AI Logic) pour l’import par IA ;
- **Google Play** (paiements et abonnements) ;
- **Google Drive** ou **ton serveur WebDAV**, uniquement si tu actives la sauvegarde correspondante.

Ces prestataires peuvent traiter des données **en dehors de l’Union européenne**, notamment aux États-Unis. Ces transferts sont encadrés par des garanties appropriées (Data Privacy Framework UE–États-Unis et/ou clauses contractuelles types de la Commission européenne), conformément aux conditions de Google.

## 6) Import par IA : photos, liens et texte
Lorsque tu déclenches un import par IA :
- les **photos** (ou le **texte de la publication** et son **URL** pour un import par lien) sont envoyés à **Google Gemini** via **Firebase AI Logic** pour en extraire une recette structurée ;
- **l’éditeur ne conserve aucune copie** de ces contenus sur ses serveurs ; la recette obtenue et les photos restent sur ton appareil ;
- Google traite ces contenus pour générer la réponse, selon ses propres conditions applicables à l’API Gemini ;
- le résultat peut contenir des erreurs : vérifie-le et corrige-le avant usage (quantités, allergènes, cuisson, etc.).

> Conseil : évite de photographier des éléments contenant des informations personnelles (visages, adresses, documents officiels).

## 7) Durées de conservation
- **Recettes et contenu saisi** : sur ton appareil, jusqu’à ce que tu les supprimes ou désinstalles l’application.
- **Photos et textes envoyés à l’IA** : non conservés par l’éditeur ; traités par Google le temps de générer la réponse, selon ses conditions.
- **Compte et compteurs d’utilisation** (si connexion Google) : jusqu’à la suppression de ton compte sur demande (voir section 8).
- **Données de diagnostic (Crashlytics)** : 90 jours.
- **Statistiques d’usage (Analytics)** : selon la durée de conservation configurée dans Google Analytics (entre 2 et 14 mois).
- **Achats et abonnements** : selon les règles de Google Play et les obligations légales (comptables notamment).
- **Sauvegardes Drive / WebDAV** : tant que tu les conserves sur le service choisi.

## 8) Tes droits
Conformément au RGPD et à la loi Informatique et Libertés, tu disposes des droits d’**accès**, de **rectification**, d’**effacement**, de **limitation**, d’**opposition**, de **portabilité**, du droit de **retirer ton consentement** à tout moment, et du droit de définir des directives relatives au sort de tes données après ton décès.

Pour exercer ces droits, ou **demander la suppression de ton compte et des données associées** : **itadaki.app@gmail.com**. Indique l’adresse e-mail de ton compte Google si tu t’es connecté. Nous répondons dans un délai d’un mois.

Tu peux aussi, à tout moment et sans nous contacter :
- te **déconnecter** de ton compte Google dans l’application ;
- supprimer tes recettes ou **désinstaller l’application** pour effacer les données locales ;
- révoquer l’accès d’Itadaki à ton compte Google depuis les paramètres de ton compte Google (Sécurité → Applications tierces).

Si tu estimes que tes droits ne sont pas respectés, tu peux introduire une réclamation auprès de la **CNIL** (www.cnil.fr).

## 9) Mineurs
L’application s’adresse à un public général. Si tu as moins de 15 ans, demande l’accord d’un parent avant de te connecter avec Google ou de souscrire un abonnement.

## 10) Sécurité
Nous mettons en œuvre des mesures raisonnables pour protéger tes données : chiffrement des échanges (HTTPS), chiffrement local du mot de passe WebDAV, vérification App Check, et minimisation des données collectées. Aucun système n’est toutefois infaillible.

## 11) Modifications
Cette politique peut être mise à jour, notamment en cas d’évolution des fonctionnalités. La date de « Dernière mise à jour » sera modifiée en conséquence et, en cas de changement important, tu en seras informé dans l’application.
