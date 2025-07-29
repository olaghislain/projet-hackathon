# AI4CKD - Plateforme de gestion des maladies rénales chroniques

## Présentation

AI4CKD est une plateforme web destinée à la gestion et au suivi des patients atteints de maladies rénales chroniques (CKD). Elle permet aux professionnels de santé de consulter, ajouter et suivre les patients, leurs consultations, alertes médicales et de générer des rapports PDF.

## Fonctionnalités principales

- Gestion des patients (création, édition, liste, détails)
- Suivi des consultations et des données cliniques
- Système d’alertes médicales (avec niveaux de sévérité)
- Génération de rapports médicaux PDF
- Tableau de bord avec statistiques et alertes actives
- Interface utilisateur moderne avec React, TailwindCSS et Vite

## Structure du projet

```
.
├── client/         # Frontend React (Vite, TypeScript)
│   └── src/
│       ├── components/
│       ├── hooks/
│       ├── lib/
│       ├── pages/
│       └── ...
├── server/         # Backend Node.js (Express, Drizzle ORM)
│   ├── services/
│   ├── db.ts
│   ├── routes.ts
│   └── ...
├── shared/         # Schémas partagés (Zod)
├── attached_assets/ # Fichiers PDF générés ou importés
├── .config/        # Configuration (Semgrep, sécurité)
└── ...
```

## Installation

### Prérequis

- Node.js >= 18
- npm ou yarn
- (Optionnel) PostgreSQL ou autre base compatible avec Drizzle ORM

### 1. Cloner le dépôt

```sh
git clone <url-du-repo>
cd <nom-du-repo>
```

### 2. Installer les dépendances

```sh
npm install
# ou
yarn install
```

### 3. Configurer les variables d’environnement

Copie le fichier `.env.example` en `.env` et adapte les variables à ton environnement.

### 4. Démarrer le backend

```sh
cd server
npm run dev
```

### 5. Démarrer le frontend

Dans un autre terminal :

```sh
cd client
npm run dev
```

## Scripts utiles

- `npm run build` : Build du frontend pour la production
- `npm run lint` : Lint du code
- `npm run test` : Lancer les tests unitaires

## Technologies utilisées

- **Frontend** : React, TypeScript, Vite, TailwindCSS, React Query
- **Backend** : Node.js, Express, Drizzle ORM, PDFKit
- **Validation** : Zod
- **Sécurité** : Semgrep (règles dans [.config/.semgrep/semgrep_rules.json](.config/.semgrep/semgrep_rules.json))

## Génération de rapports PDF

La génération des rapports PDF est gérée côté serveur via [`server/services/pdf-service.ts`](server/services/pdf-service.ts).

## Contribution

1. Fork le projet
2. Crée une branche (`git checkout -b feature/ma-feature`)
3. Commit tes modifications (`git commit -am 'feat: ma feature'`)
4-push origin feature/ma-feature`)
5. Ouvre une Pull Request

Merci de respecter la structure du code et les conventions existantes. Toute contribution est la bienvenue !

## Licence

Ce projet est sous licence MIT.

## Auteurs

- [Gael DANSOU]


---

Pour toute question ou suggestion, n’hésite pas à ouvrir une issue ou à contacter les mainteneurs.
