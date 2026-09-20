---
title: "Le coût réel de l'IA d'abord"
date: 2026-09-08
slug: "the-real-cost-of-ai-first"
tags: ["IA d'abord", "coûts", "stratégie", "opérations"]
status: "published"
excerpt: "L'inférence est le poste le moins cher. La facture de l'IA d'abord tient surtout à l'évaluation, à la revue humaine, à la maintenance et à la conformité — et la plupart des budgets n'en tiennent pas compte. Voici l'arithmétique qui détermine si une fonctionnalité d'IA mérite d'être développée."
---

La première fonctionnalité d'IA qu'une entreprise met en ligne coûte généralement peu. Une clé d'API, un prototype, une démonstration qui fait mouche en réunion de direction. C'est la deuxième année que les dépenses arrivent — et c'est rarement ce que quiconque avait budgété.

## La facture n'est pas celle de l'inférence

Les appels aux modèles sont le coût le plus visible et, de plus en plus, le moins important. Pour un niveau de capacité donné, les prix ont baissé d'environ un ordre de grandeur par an ces trois dernières années, et la concurrence continue de les tirer vers le bas. Pendant ce temps, les coûts qui entourent l'appel au modèle restent stables ou augmentent :

- **L'évaluation et la plomberie des données.** Journaliser chaque interaction avec l'étiquette de son résultat, maintenir des jeux de référence et mettre en place des barrières de non-régression. Sans cela, impossible de distinguer une amélioration d'un bruit de fond — et vous le paierez en régressions mises en production.
- **La revue humaine et l'escalade.** Partout où une mauvaise réponse coûte cher, une personne doit vérifier la sortie. Ce travail n'est pas gratuit et ne diminue pas simplement parce que le modèle s'est amélioré ; il se déplace.
- **La maintenance face au renouvellement des modèles.** Les fournisseurs retirent des versions, modifient les paramètres par défaut et déprécient des options. Chacun de ces événements déclenche de nouveaux tests, des ajustements de prompts et parfois une requalification complète de la fonctionnalité.
- **La revue de conformité et de sécurité.** Localisation et conservation des données, listes de sous-traitants, accords de traitement des données, et désormais des questions propres à l'IA posées par les clients et les magasins d'applications. Ce travail est ponctuel pour chaque fonctionnalité, mais il se répète à chaque fournisseur et à chaque juridiction.
- **Le support d'un logiciel probabiliste.** Les utilisateurs signalent des problèmes difficiles à reproduire, car la réponse diffère à chaque fois. Les outils et les procédures de support doivent être réécrits pour cette réalité.
- **Le coût de l'erreur.** Un prix halluciné, un résumé erroné dans une revue de contrat, une sortie choquante affichée à un client. Ces éléments n'apparaissent jamais dans un modèle de coûts, mais c'est pour eux que plusieurs fonctionnalités d'IA ont été discrètement retirées.

Aucun de ces postes n'apparaît dans une comparaison de « coût par million de tokens », et c'est précisément pour cela qu'ils passent facilement inaperçus.

## Ce que disent les données sur le retour sur investissement

La distribution des gains n'est pas uniforme. Deux types de preuves coexistent sur le même marché.

D'un côté, des mesures contrôlées montrent de vrais gains sur des tâches étroites et à fort volume : une expérience randomisée menée chez GitHub en 2023 a constaté que les développeurs terminaient une tâche 55.8% plus vite avec un assistant d'IA (arXiv:2302.06590), et une étude sur les outils de support client a relevé une hausse d'environ 14% en moyenne du nombre de problèmes résolus par heure, et d'environ 34% pour les collaborateurs les moins expérimentés (Brynjolfsson, Li et Raymond, NBER working paper 31161).

De l'autre, les résultats au niveau d'un portefeuille de projets sont médiocres. Une étude du MIT publiée en 2025 sur les pilotes d'IA générative en entreprise a rapporté que la grande majorité n'avait produit aucun impact mesurable sur le compte de résultat, et une enquête de S&P Global de 2024 a constaté qu'une large part des entreprises avaient abandonné la plupart de leurs initiatives d'IA. Ces deux constats doivent être lus comme des approximations d'une réalité désordonnée plutôt que comme des mesures précises — mais ils vont dans le même sens.

La conciliation n'est pas compliquée. Les gains apparaissent là où un flux de travail dispose d'un indicateur mesurable, d'un volume suffisant pour compter et d'une sortie qu'une personne peut vérifier rapidement. Les pertes se concentrent là où l'indicateur n'a jamais été défini, où le volume était faible, ou là où la fonctionnalité a été construite parce que c'était possible, et non parce que quelqu'un répondait du résultat.

## L'arithmétique qui tranche

Avant de construire, écrivez trois chiffres :

1. **Le coût par tâche** avec le modèle, en incluant les nouvelles tentatives, le travail de revue et la maintenance amortie.
2. **Le coût par tâche aujourd'hui**, tout compris — salaires, outils, correction des erreurs.
3. **Le coût d'une erreur**, et la question de savoir si une étape de revue humaine le borne.

Une fonctionnalité d'IA est défendable lorsque le premier chiffre est nettement inférieur au deuxième, une fois les coûts de revue inclus, que le troisième est borné par un processus réellement en place, et que le volume est suffisamment élevé pour que l'écart se cumule. Si le troisième chiffre n'est pas borné — une décision qui peut blesser quelqu'un, enfreindre une réglementation ou détruire une relation — alors l'étape de revue n'est pas facultative et doit être intégrée au calcul dès le départ.

Deux conséquences en découlent. Premièrement, certains des meilleurs projets d'IA sont modestes : ils remplacent une tâche étroite, répétitive et à fort volume. Deuxièmement, certaines fonctionnalités doivent être refusées. Ce n'est pas une position anti-IA ; c'est ce que fait un budget.

## Là où l'IA est simplement le mauvais outil

- **La logique déterministe.** Calcul de taxes, règles d'éligibilité, arithmétique de stock. Les règles sont moins chères, plus rapides, auditables et stables. Y ajouter un modèle les dégrade, sans les moderniser.
- **Un faible volume.** Si une tâche s'exécute cinquante fois par mois, le coût fixe d'un jeu d'évaluation, d'un processus de revue et d'un responsable de la maintenance ne sera jamais rentabilisé.
- **De mauvaises données d'entrée.** Si les données sous-jacentes sont incomplètes ou si le processus n'est pas défini, un modèle produira à grande échelle des absurdités énoncées avec assurance. Corrigez d'abord les données ; le modèle n'a rien avec quoi travailler.
- **Un coût d'erreur non borné sans revue.** Lorsqu'une personne doit de toute façon approuver chaque sortie, demandez-vous honnêtement si le modèle a fait gagner quoi que ce soit, ou s'il a simplement déplacé le travail.

## Budgéter honnêtement

Trois habitudes séparent les équipes qui obtiennent de la valeur de celles qui reçoivent des factures.

**Fixez un plafond avant de construire.** Un coût maximal par tâche réussie, et une hypothèse de volume. Si la fonctionnalité ne peut pas passer sous ce plafond à ce volume, elle n'est pas mise en production — quelle que soit la qualité de la démonstration.

**Suivez le coût par résultat réussi, pas le coût par appel.** Un modèle bon marché qui échoue une fois sur trois est cher. Un modèle performant réservé aux 20% de cas difficiles, un petit modèle traitant le reste, constitue généralement l'architecture la moins chère disponible.

**Écrivez le critère d'arrêt à l'avance.** « Si la qualité n'atteint pas X sur notre jeu d'évaluation à la date Y, nous arrêtons. » Presque toutes les initiatives d'IA devenues des centres de coûts permanents ont commencé comme des pilotes que personne n'avait le pouvoir d'arrêter.

Les prix continueront de baisser, et c'est utile — mais une inférence moins chère ne réduit ni le travail de revue, ni la maintenance, ni le coût d'une mauvaise réponse. L'IA d'abord n'est pas la décision d'utiliser l'IA partout. C'est la discipline consistant à trouver les endroits où les chiffres tiennent réellement, et à avoir le cran de le dire lorsqu'ils ne tiennent pas.

*À lire également : [« L'IA d'abord » est une discipline, pas un slogan](/blog/fr/ai-first-is-a-discipline).*
