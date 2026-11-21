# Harada Coach

*[English version](README.md)*

Un skill pour Claude qui t'accompagne pas à pas dans la **méthode Harada** : transformer un objectif ambitieux en plan d'action concret, puis le tenir dans la durée grâce à des routines, un journal quotidien et une revue mensuelle.

Le skill ne remplit pas les formulaires à ta place. Il te pose une question à la fois, te pousse à être concret, te propose des idées quand tu bloques, puis met tes réponses en forme dans des documents prêts à l'emploi.

> **Langue :** le skill est rédigé en anglais, mais le coach te répond dans la langue que tu utilises. Écris-lui en français, il te répondra en français. Les titres des documents générés peuvent rester en anglais.

## À quoi ça sert

- Clarifier un objectif flou jusqu'à le rendre **mesurable et daté**.
- Comprendre **pourquoi** tu le veux vraiment, et ce qui t'a fait réussir ou échouer par le passé.
- Anticiper les obstacles avant qu'ils arrivent.
- Découper l'objectif en **8 domaines et 64 actions** (la grille Open Window 64).
- Passer à l'action dès le lendemain avec 10 tâches datées et 10 routines.
- Garder le cap grâce au journal quotidien et à la revue de chaque mois.

Ça marche pour un objectif personnel (santé, sport, apprentissage, finances) comme pour un objectif professionnel ou d'équipe.

## L'origine de la méthode

La méthode a été créée par **Takashi Harada**, professeur d'éducation physique dans un collège d'Osaka. Dans un établissement réputé difficile, il a amené ses élèves au plus haut niveau national en athlétisme, en misant sur une idée simple : apprendre à chacun à devenir **autonome** (*self-reliant*), c'est-à-dire capable de se fixer un but et de se coacher seul.

Il a ensuite formalisé son approche et l'a enseignée à des entreprises japonaises. Norman Bodek l'a fait connaître en Occident avec le livre *The Harada Method*.

Elle est devenue célèbre grâce au joueur de baseball **Shohei Ohtani**, qui a rempli une grille Open Window 64 au lycée pour viser une sélection en premier tour de draft.

> Source : Takashi Harada et Norman Bodek, *The Harada Method, 2nd Edition: The Spirit of Self-Reliance*, PCS Press, 2024. Ce skill reformule la méthode et ne reproduit pas le livre.

## Ce que le skill produit

Un dossier `harada/<ton-objectif>/` contenant :

| Document | Rôle |
|---|---|
| `0-Dashboard.md` | Tableau de bord : objectif, paliers, jalons, tâches, routines, avancement |
| `1-Self-assessment 33 qualities.md` | Où tu en es sur les 33 qualités d'autonomie |
| `2-Long-term goal form.md` | Le formulaire objectif long terme complet |
| `3-Open Window 64 chart.md` | La grille 9×9 : objectif au centre, 8 domaines, 64 actions |
| `4-Routine check sheet - AAAA-MM.md` | La feuille de routines du mois, à cocher chaque jour |
| `5-Diary/` | Le journal quotidien |
| `6-Monthly review - template.md` | La trame de la revue de fin de mois |

Les fichiers sont en Markdown : ils s'ouvrent dans n'importe quel éditeur, et s'intègrent bien dans Obsidian.

## Installation

### Claude Code

Cloner le dépôt dans ton dossier de skills personnels :

```bash
git clone https://github.com/ojtouch/harada-coach ~/.claude/skills/harada-coach
```

Sous Windows (PowerShell) :

```powershell
git clone https://github.com/ojtouch/harada-coach "$env:USERPROFILE\.claude\skills\harada-coach"
```

Pour le réserver à un seul projet, le cloner plutôt dans `.claude/skills/harada-coach` à la racine du projet.

### Claude.ai ou Claude Desktop

Télécharger le dépôt en ZIP (bouton **Code** puis **Download ZIP**), puis l'importer dans **Paramètres > Capacités > Skills**.

## Utilisation

Lance le skill avec une commande ou simplement en parlant de ton objectif :

| Commande | Ce qui se passe |
|---|---|
| `/harada-coach` ou « j'ai un objectif » | Nouvel objectif : la séance complète (60 à 90 minutes, découpable en plusieurs fois) |
| `/harada-coach assessment` | Uniquement le diagnostic des 33 qualités d'autonomie |
| `/harada-coach diary` | Le journal du jour : bilan, routines cochées, plan du lendemain et retour de coach |
| `/harada-coach review` | La revue du mois : taux de routines, jalons, nouvelles tâches et routines |
| `/harada-coach team` | Décliner un objectif collectif pour chaque membre d'une équipe |

### Déroulé d'une séance « nouvel objectif »

1. Diagnostic d'autonomie (facultatif, conseillé la première fois)
2. Objectif central, 4 paliers et jalons
3. Service quotidien, à la maison et au travail
4. Raisons et valeurs, sous 4 angles
5. Analyse des succès, échecs et obstacles
6. Les 8 domaines d'action
7. Les 64 actions, notées par impact et effort
8. Plan de démarrage : 10 tâches et 10 routines
9. Mental et soutien
10. Rituels de suivi
11. Génération des documents

Si tu t'arrêtes en cours de route, l'avancement est enregistré dans le tableau de bord pour reprendre au bon endroit.

## Structure du dépôt

```
harada-coach/
├── SKILL.md        # Instructions du coach
├── references/     # Méthode détaillée, phase par phase, et garde-fous
└── templates/      # Modèles des documents générés
```

## Licence

MIT. Voir [LICENSE](LICENSE).
