# NextJS folder feature first structure

Cette structure de projet consiste à organiser le code en modules plutôt qu'en couches, ce qui facilite la maintenance et l'évolutivité de l'application.

### Description des répertoires

#### Répertoire `src`

Le répertoire src est utilisé pour stocker le code source de l'application, organisé par modules (features) et partagé (chore). 

Il contient les sous-dossiers suivants :

* `app`: décrit plus haut
* `features` : contient les fonctionnalités de l'application, organisées par dossier.
* `chore` : contient des composants, des services, des types et des utilitaires partagés entre les fonctionnalités de l'application.

Chaque fonctionnalité (feature) est organisée en sous-dossiers contenant les `composants`, `les pages`, `les services`, `le store et les types` spécifiques à cette fonctionnalité. Chaque fonctionnalité a également un fichier index.ts qui exporte les éléments nécessaires à l'utilisation de la fonctionnalité dans l'application.

#### Répertoire `app`

Il s'agit du [nouveau répertoire](https://nextjs.org/docs/getting-started/project-structure#app-routing-conventions) introduit dans [Next 13](https://nextjs.org/blog/next-13) avec de nouvelles fonctionnalités en termes de [routing](https://nextjs.org/docs/app/building-your-application/routing#the-app-router), layouts, loading states, error handling, etc. Ce répertoire est utilisé pour stocker pour tirer parti de Nextjs 13. 

Il contient les sous-répertoires suivant la convention de routage de Next 13 et les fcihiers racines du framework.


#### Arborescence

```bash
src
├── app
│   ├── dashboard
│   ├── favicon.ico
│   ├── globals.css
│   ├── layout.tsx
│   ├── login
│   ├── page.module.css
│   ├── page.tsx
│   ├── projects
│   ├── settings
│   └── todos
│       └── page.tsx
├── core
│   ├── components
│   ├── config
│   │   ├── routes
│   │   │   └── index.ts
│   │   └── theme
│   │       └── index.ts
│   ├── context
│   │   └── __tests__
│   ├── data
│   ├── hooks
│   │   ├── __tests__
│   ├── layouts
│   ├── lib
│   ├── services
│   ├── styles
│   └── utils
│       └── __tests__
└── features
    ├── authentication
    │   ├── components
    │   ├── hooks
    │   ├── index.ts
    │   ├── services
    │   └── types
    ├── projects
    │   ├── components
    │   ├── index.ts
    │   └── services
    ├── settings
    │   ├── components
    │   ├── context
    │   ├── hooks
    │   ├── index.ts
    │   └── services
    └── todos
        ├── assets
        │   └── image.jpg
        ├── components
        ├── context
        ├── index.tsx
        └── services
```




En résumé, cette structure de projet Next.js est une approche modulaire permettant de séparer clairement les différentes parties de l'application et de faciliter la maintenance et l'évolutivité de l'application.