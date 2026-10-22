# VKT Cart Lock

[English](../README.md) | [中文](README_zh.md) | [Deutsch](README_de.md) | [Español](README_es.md) | [日本語](README_ja.md) | Français

**Un verrou de réflexion strict pour votre panier.** Cliquez sur le paiement et le minuteur démarre. Le paiement reste bloqué jusqu'à la fin du minuteur, puis s'ouvre tout seul.

Également connu sous le nom de **冷静锁** en chinois.

> Chromium · Manifest V3 · 6 langues · Aucun suivi · Local d'abord

---

## Pourquoi VKT Cart Lock ?

La plupart des outils contre les « achats impulsifs » laissent une porte ouverte : répéter, ignorer, déverrouiller en avance. Pas VKT Cart Lock. Le but est de protéger la décision que vous avez déjà prise de la version de vous qui fixe un bouton de paiement à minuit.

- **Pas de répétition, pas d'ignorance, pas de déverrouillage anticipé.** Désinstaller l'extension est le seul moyen de contourner.
- **Le minuteur continue hors de la page.** Fermez l'onglet, redémarrez le navigateur, revenez demain : le verrou est toujours là.
- **L'expiration est silencieuse par défaut.** Le paiement se rouvre simplement. Premium peut ajouter une dernière confirmation.
- **Un achat terminé démarre un nouveau verrou.** Acheter ne remet pas l'habitude à zéro.
- **Local d'abord.** Minuteurs, réglages, messages et statistiques restent dans votre navigateur. Pas d'analyse, pas de publicité, l'historique de navigation ne quitte pas l'appareil.

---

## Fonctionnalités

### Gratuit

| Fonctionnalité | Description |
|---------|-------------|
| Verrou strict du paiement | Clics, liens de paiement, soumissions de formulaires et pages de paiement sont interceptés |
| 24 présélections de sites + détection générique | Règles ajustées à la main pour les grandes boutiques, plus des solutions de repli par texte et sélecteurs partout ailleurs |
| Présélections de réflexion | 1 heure, 6 heures, 24 heures ou 72 heures |
| Minuteurs par site | Un verrou actif par site, lancé par le premier clic de paiement |
| Messages personnalisés | Jusqu'à 20 lignes, en affichage fixe, rotatif ou aléatoire |
| Trois sons | Sourd, carillon ou doux, plus un interrupteur muet |
| Exemption des petites commandes | Laissez passer l'essentiel sous un montant choisi |
| Liste autorisée et sites à verrouillage forcé | Ignorez une boutique de confiance, ou forcez la protection sur une petite boutique indépendante |
| Période calme des soldes | Black Friday, Prime Day et le Double 11 prolongent automatiquement la réflexion à 72 heures |
| Réglages protégés par mot de passe | Un code PIN de 4 à 8 caractères protège la page des réglages |
| Étiquettes d'émotion | Étiquetez le moment — tard la nuit, soldes, en colère, ennuyé, je le veux c'est tout |
| Signalement des blocages erronés | Marquez un faux positif et excluez cet élément la prochaine fois |
| Compte à rebours sur l'icône | L'icône de la barre d'outils affiche les heures ou minutes restantes |
| Registre de base | Total des paiements bloqués et montant retenu, mois en cours inclus |

### Premium

| Fonctionnalité | Description |
|---------|-------------|
| Réflexions personnalisées | De 10 minutes à 30 jours |
| Minuteurs par article | Un verrou par produit au lieu d'un par site |
| Démarrage à l'ajout au panier | Le minuteur démarre quand un article entre dans le panier |
| Messages illimités | Limités uniquement par le budget de synchronisation entre appareils (environ 60 lignes) |
| Heures de silence | Aucun son pendant les heures choisies ; le verrou fonctionne toujours |
| Confirmation après expiration | Un dernier clic « je le veux toujours » après la fin du minuteur |
| Synchronisation entre appareils | Réglages et minuteurs suivent votre compte Chrome / Edge |
| Rapports sur 12 mois | Tendance mensuelle, classement des sites et répartition des émotions |
| Export CSV | Emportez l'historique dans un tableur |
| Sauvegarde JSON | Export et import complets des réglages, messages, minuteurs et statistiques |

L'activation Premium est facultative. Tout ce qui est au-dessus de la ligne Premium fonctionne sans compte ni clé de licence.

---

## Comment ça marche

1. **Premier clic de paiement.** La protection intercepte le clic, démarre le minuteur et affiche l'écran de verrouillage. La commande n'est pas envoyée.
2. **Chaque tentative suivante.** Le paiement reste bloqué et la superposition décompte le temps restant.
3. **Le minuteur fait foi.** Il vit dans le stockage de l'extension, pas dans l'onglet. Fermer la page, rouvrir la boutique ou redémarrer le navigateur ne le raccourcit pas.
4. **Quand le temps est écoulé.** Le verrou se libère en silence et le paiement est à nouveau autorisé. Les utilisateurs Premium peuvent exiger d'abord un clic de confirmation.
5. **Après un achat.** Une commande terminée démarre une nouvelle réflexion, si bien que l'achat suivant passe par la même pause.

La protection n'agit que dans la page. Elle n'accroche jamais de requêtes réseau et ne touche jamais aux iframes de paiement ni aux pages des prestataires de paiement (Stripe, PayPal, Adyen, checkout.com, Braintree et hôtes similaires sont exclus).

---

## Installation

1. Ouvrez `chrome://extensions/` dans Chrome ou `edge://extensions/` dans Edge.
2. Activez le **mode développeur**.
3. Cliquez sur **Charger l'extension non empaquetée** et sélectionnez ce dossier.
4. Épinglez l'extension à la barre d'outils.

Pour une version empaquetée, utilisez le zip dans `publish/` ou chargez le dossier manuellement pendant le développement.

---

## Utilisation

- **Définissez une réflexion.** Ouvrez les options de l'extension et choisissez une présélection, ou une durée personnalisée avec Premium.
- **Écrivez votre propre phrase.** L'écran de verrouillage peut afficher vos mots au lieu des citations intégrées. Le mode rotatif évite qu'elle devienne un papier peint.
- **Ajoutez des règles.** Autorisez un site d'épicerie, forcez le verrou sur une petite boutique ou exemptez les commandes sous un montant donné.
- **Regardez l'icône.** Le compte à rebours de la barre d'outils est le rappel silencieux que le verrou est toujours actif.
- **Consultez le registre.** Le tableau de bord montre ce qui a été bloqué, ce que cela aurait coûté, quels sites et humeurs déclenchent le plus de paiements, et une tendance sur 12 mois.
- **Sauvegardez (Premium).** Utilisez l'export JSON avant de changer de machine. La synchronisation restaure les réglages et les minuteurs, mais les statistiques locales ne voyagent pas.

Désinstaller l'extension efface ses données locales. Si la synchronisation Premium est activée, les messages et réglages reviennent après réinstallation ; les statistiques et l'historique local, non.

---

## Sites pris en charge

Les présélections ajustées à la main couvrent 24 boutiques, dont Amazon, eBay, Etsy, Walmart, Target, Best Buy, Home Depot, Lowe's, Newegg, Wayfair, Mercari, AliExpress, Temu, Alibaba, DHgate, Shopee, Lazada, Rakuten, SHEIN, TikTok Shop, bol.com, Allegro, Otto et Cdiscount.

Toute autre boutique est couverte par la correspondance générique des textes et sélecteurs de boutons de paiement. Si un site change son balisage, la note d'auto-vérification du menu contextuel vous indique que la protection mérite peut-être un nouvel examen.

---

## Navigateurs pris en charge

| Navigateur | Statut |
|---------|--------|
| Google Chrome | Entièrement pris en charge |
| Microsoft Edge | Entièrement pris en charge |
| Autres navigateurs basés sur Chromium | Devrait fonctionner |

---

## Données et confidentialité

- **Stocké localement :** réglages, minuteurs, statistiques, notes d'auto-vérification, le PIN facultatif des réglages (hachage SHA-256 salé uniquement) et l'enregistrement de licence Premium.
- **Synchronisé (Premium, sur adhésion) :** réglages, messages personnalisés et enregistrements légers de minuteurs via `chrome.storage.sync`. Le PIN des réglages n'est jamais synchronisé.
- **Envoyé au serveur de licences :** uniquement lors de l'activation, de la validation ou de la désactivation de Premium — la clé de licence, un identifiant d'installation aléatoire, l'ID du plugin et des métadonnées de base du navigateur (version du navigateur, langue, fuseau horaire, agent utilisateur).
- **Non collecté :** contenu des pages, historique de navigation, contenu du panier, informations de paiement, frappes ou analyses.

Il n'y a ni compte, ni publicité, ni vente de données. Désinstaller l'extension supprime les données locales ; les enregistrements de licence côté serveur peuvent être supprimés en désactivant d'abord la licence.

Consultez [privacy-policy.html](../privacy-policy.html) pour la politique complète.

---

## Autorisations

| Autorisation | Pourquoi elle est nécessaire |
|------------|------------------|
| `storage` | Enregistrer réglages, minuteurs et statistiques localement ; les synchroniser pour Premium |
| `alarms` | Garder le compte à rebours précis et libérer les verrous à temps |
| `notifications` | Afficher une notification locale de bureau quand un nouveau verrou démarre |
| `host_permissions: <all_urls>` | Détecter un bouton de paiement sur n'importe quelle boutique, car les boutiques utilisent des domaines arbitraires |
| `host_permissions: api.annmax1983.com` | Activer et valider une licence Premium facultative |

Le script de contenu s'exécute dans toutes les frames pour attraper les boutons de paiement dans les widgets des boutiques, mais les hôtes des prestataires de paiement sont explicitement exclus.

---

## Langues

English, 简体中文, 日本語, Deutsch, Español et Français. L'interface, les citations intégrées et les descriptions des boutiques sont localisées.

---

## Licence

VKT Cart Lock est une extension commerciale. Le niveau Gratuit est utilisable sans licence. Les fonctionnalités Premium nécessitent une clé de licence active de [annmax1983.com](https://www.annmax1983.com/).
