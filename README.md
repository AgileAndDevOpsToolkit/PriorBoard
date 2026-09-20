# PriorBoard

🔗 Application directement accessible en ligne : **https://agileanddevopstoolkit.github.io/PriorBoard/**

> ⚠️ **Confidentialité et sécurité des données**
> PriorBoard ne stocke **aucune donnée sur un serveur**. Tout ce que vous saisissez (items, titre du tableau, historique des battles) reste **exclusivement dans le `localStorage` de votre navigateur**, sur votre machine. L'application n'introduit donc aucun risque de sécurité côté serveur : vous êtes entièrement responsable de vos données.
>
> Pensez à **télécharger régulièrement un fichier de sauvegarde (JSON)** via le bouton dédié : en cas de changement de navigateur, de nettoyage du cache ou de perte des données locales, seul ce fichier vous permettra de retrouver votre tableau.

## Qu'est-ce que PriorBoard ?

PriorBoard est un outil simple pour **prioriser une liste d'items** (idées, sujets, backlog...) en les comparant deux à deux façon "battle", et en calculant un classement basé sur le score **ELO** (le même système que pour classer les joueurs d'échecs).

Plutôt que de noter chaque item dans l'absolu, vous répondez à des choix simples ("A ou B ?"), et le classement se construit progressivement au fil des duels.

## Fonctionnalités

- **Ajout d'items** en masse (un par ligne) ou via import d'un fichier.
- **Mode Battle** : duels aléatoires entre deux items actifs, mise à jour du score ELO après chaque choix.
- **Classement** trié par score ELO, avec nombre de battles disputées par item.
- **Édition du titre d'un item** directement dans la liste (icône crayon au survol).
- **Marquer un item comme terminé** ou **le désactiver** (pour l'exclure temporairement des battles) sans le supprimer.
- **Titre de tableau** optionnel, éditable dans la barre du haut.
- **Export / Import JSON** : téléchargez vos données ou importez une sauvegarde précédente.
- Aucune inscription, aucun compte, aucun serveur : tout fonctionne côté navigateur.

## Utilisation

1. Ouvrez [https://agileanddevopstoolkit.github.io/PriorBoard/](https://agileanddevopstoolkit.github.io/PriorBoard/).
2. Ajoutez vos items dans la zone "Ajouter des items".
3. Passez sur l'onglet **Battle** et répondez aux duels proposés.
4. Consultez le classement dans l'onglet **Classement**.
5. Téléchargez régulièrement une sauvegarde JSON via le bouton de téléchargement dans la barre du haut.

## Développement local

Le projet est une application statique (un unique fichier [index.html](index.html)), sans dépendance ni étape de build. Pour la servir localement, par exemple avec PHP :

```bash
php -S 0.0.0.0:8000
```

Puis ouvrez `http://localhost:8000` dans votre navigateur.
