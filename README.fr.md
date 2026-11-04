# AskGSC — Google Search Console dans ChatGPT et Claude grâce à MCP

**AskGSC permet d'analyser ses données Google Search Console directement dans un assistant IA compatible MCP.** Le service héberge un serveur MCP (Model Context Protocol) donnant accès à **11 outils de lecture seule** : performances SEO, requêtes, pages, comparaisons temporelles, opportunités de CTR, inspection d'URL et sitemaps.

**Site :** [askgsc.app](https://askgsc.app/) · **Inscription :** [Connecter Google Search Console](https://askgsc.app/connect) · **Tarifs :** [Free et Pro](https://askgsc.app/pricing)

## Connexion

1. Connectez votre compte Google sur [AskGSC](https://askgsc.app/connect) et autorisez l'accès **en lecture seule** aux propriétés Search Console auxquelles vous avez déjà accès.
2. Dans ChatGPT, Claude ou un autre client compatible avec les serveurs MCP distants personnalisés, ajoutez un connecteur MCP.
3. Renseignez cette URL et terminez l'autorisation OAuth :

```text
https://mcp.askgsc.app/mcp
```

4. Demandez par exemple : « Pour [PROPRIÉTÉ], quelles pages ont perdu le plus de clics sur les 28 derniers jours complets par rapport à la période précédente ? »

**Important :** la disponibilité de l'ajout de connecteurs personnalisés dépend du client IA, de l'abonnement et de l'espace de travail. Aucun serveur local ou export CSV à maintenir.

## Ce que l'on peut analyser

- Clics, impressions, CTR et position moyenne.
- Requêtes et pages par période, pays ou appareil.
- Progressions, baisses et opportunités SEO à investiguer.
- Pages associées aux mêmes requêtes (sans conclure automatiquement à une cannibalisation).
- Dernier état d'indexation connu de Google, canonicals et avertissements de sitemaps.

## Offre

**14 jours d'essai complet sans CB**, puis Free avec **20 crédits MCP mensuels par défaut** (quota affiché dans le compte). **Pro : 4,99 €/mois** sans plafond mensuel AskGSC pendant l'abonnement, sous réserve des limites des API et du service. L'essai ne déclenche aucun paiement automatique. [Tarifs à jour](https://askgsc.app/pricing).

## Documentation détaillée (EN)

[Premiers pas](docs/getting-started.md) · [ChatGPT](docs/chatgpt.md) · [Claude](docs/claude.md) · [11 outils MCP](docs/mcp-tools.md) · [Prompts SEO](docs/prompts.md) · [Limites et sécurité](docs/privacy-and-limitations.md)

Le dépôt contient de la **documentation**, pas le code source d'AskGSC. AskGSC est un service indépendant, sans affiliation à Google, OpenAI ou Anthropic.
