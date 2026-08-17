# Réveils Train

PWA locale qui calcule les 4 heures d'alarme à régler manuellement
à partir de l'heure de départ du train du lendemain.

## Fonctionnement

1. Sélectionne le jour de la semaine
2. Entre l'heure du train
3. Ajuste la marge avant le train si besoin (défaut : 30 min)
4. Les 4 heures s'affichent → tu les saisis sur ta montre et ton téléphone

**Séquence :** Montre 1 → +5 min → Montre 2 → +5 min → Montre 3
→ +15 min → Téléphone → ≥ 30 min → Train

L'heure du téléphone est arrondie aux 5 minutes inférieures.
Les alarmes de la montre en découlent par soustraction.

## Installation sur le téléphone

Ouvre `https://kiliangir.github.io/reveils-train/` dans Safari (iOS)
ou Chrome (Android), puis **Ajouter à l'écran d'accueil**.

L'app fonctionne ensuite hors-ligne.

## Technique

Un seul fichier `index.html` (CSS + JS inline), pas de dépendances, pas de build.
Service worker minimal (`sw.js`) pour le cache hors-ligne.
Données stockées uniquement en `localStorage`, rien n'est envoyé à un serveur.
