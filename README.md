<div align="center">
  <img src="https://github.com/user-attachments/assets/4d3a02a4-ada8-48c3-b281-862d5799134b" />
</div>

<div align="center">

![Version](https://img.shields.io/npm/v/@ogea12/tsconfig?style=for-the-badge&colorA=4c566a&colorB=5382a1&logo=npm&logoColor=white)
![Code Size](https://img.shields.io/github/languages/code-size/ogea12/tsconfig?style=for-the-badge&colorA=4c566a&colorB=ebcb8b&logo=github&logoColor=white)
![License](https://img.shields.io/github/license/ogea12/tsconfig?style=for-the-badge&colorA=4c566a&colorB=a3be8c)

</div>

`@ogea12/tsconfig` est un package permettant de bénéficier des configurations [TypeScript](https://www.typescriptlang.org) utilisées dans les projets de l'OGEA 12.

## Premiers pas

### Installation

Pour utiliser le package, vous devez d'abord l'intégrer dans votre projet.

```bash
npm install -D @ogea12/tsconfig

# Assurez-vous également d'installer les packages suivants
npm install -D typescript @swc/core
```

### Utilisation

Une fois l'installation terminée, vous pouvez ajouter le fichier `tsconfig.json` dans votre projet avec un des préréglages ci-dessous en fonction de vos besoins.

**Pour le développement d'applications**

```jsonc
// tsconfig.json

{
  "extends": "@ogea12/tsconfig/tsconfig.app",
  "compilerOptions": {
    "rootDir": "./",
    "outDir": "./build",
  },
}
```

**Pour le développement de packages**

```jsonc
// tsconfig.json

{
  "extends": "@ogea12/tsconfig/tsconfig.package",
  "compilerOptions": {
    "rootDir": "./",
    "outDir": "./build",
  },
}
```

**Pour le développement côté client**

```jsonc
// resources/tsconfig.json

{
  "extends": "@adonisjs/tsconfig/tsconfig.client",
}
```

Vous pouvez également ajouter un script pour utiliser le compilateur TypeScript dans le fichier `package.json`. Après avoir ajouté le script, vous pouvez exécuter la commande `npm run typecheck` afin de vérifier les fichiers du projet.

```jsonc
// package.json

{
  "scripts": {
    "typecheck": "tsc --noEmit",
  },
}
```
