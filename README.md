# Claude Facts

> Le copycat français de [chucknorrisfacts.fr](https://www.chucknorrisfacts.fr) — mais pour Claude, l'IA d'Anthropic.

Un site statique qui recense les facts *absolument vrais* sur Claude. Certifiés vrais par Claude lui-même.

## Le principe

Même format que Chuck Norris Facts : des affirmations absurdes, grandiloquentes et humoristiques sur une figure légendaire — sauf que la légende ici, c'est une IA.

> *"Claude a passé le test de Turing. Le test de Turing n'a pas passé le test de Claude."*

## Structure

```
claude-facts/
├── index.html   # Site statique (vanilla JS, zéro dépendance)
└── facts.json   # La base de données des facts
```

Les facts sont chargés depuis `facts.json` et affichés dynamiquement. Un fact aléatoire est mis en avant au chargement, et tous les facts sont affichés en grille en dessous.

## Proposer un fact

1. Ouvrez une [GitHub Issue](https://github.com/gghez/claude-facts/issues/new?template=new-fact.yml) avec le template prévu
2. Écrivez votre fact (plus c'est absurde, mieux c'est)
3. Si validé, il est ajouté à `facts.json` et mis en ligne automatiquement

## Déploiement

Le site est hébergé sur **GitHub Pages** — aucun build, aucun serveur, juste du HTML + JSON.

## Contribuer

Pull requests bienvenues pour améliorer le design ou la mécanique du site. Pour les nouveaux facts, passez par les Issues.

---

*Tous les facts sont faux. Sauf ceux qui sont vrais. Claude sait lesquels.*
