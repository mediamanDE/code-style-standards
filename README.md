# mediaman Linting and Code Style Standards for JS and TS

This repository contains rational presets for typical JavaScript or TypeScript based projects.

It is using:

- eslint (https://eslint.org/)
- prettier (https://prettier.io/)
- lint-staged (https://github.com/okonet/lint-staged#readme)
- husky (https://typicode.github.io/husky/)
- stylelint (https://stylelint.io/)

## Installation of tools

### Prettier

```
npm i -D eslint-config-prettier eslint-plugin-prettier prettier
```

### ESLint

```
npm i -D @typescript-eslint/eslint-plugin@latest eslint-config-standard@latest eslint@^7.12.1 eslint-plugin-import@^2.22.1 eslint-plugin-node@^11.1.0 eslint-plugin-promise@^4.2.1 @typescript-eslint/parser@latest
```


To get this combination of packages you can run:
```
npx eslint --init
```

with these answers:
```
✔ How would you like to use ESLint? · style
✔ What type of modules does your project use? · esm
✔ Which framework does your project use? · none
✔ Does your project use TypeScript? · Yes
✔ Where does your code run? · browser
✔ How would you like to define a style for your project? · guide
✔ Which style guide do you want to follow? · standard
✔ What format do you want your config file to be in? · JSON
```

### Husky

You can add husky to your project by:
```
npx husky-init && npm install
```

### Lint-Staged

```
npx mrm lint-staged
```

### stylelint

```
npm i -D stylelint stylelint-config-standard stylelint-config-sass-guidelines
```

## Usage in your project

### Prettier / Linting
Copy these files to your project's root directory:

```
├── .eslintrc.json
└── .prettierrc.yaml
```

You can also find some npm script examples in the package.json that can be used as a reference.

### Lint-Staged

In this example we defined a lint-staged configuration:
```
"lint-staged": {
    "*.js": "eslint --cache --fix"
  }
```

## stylelint

```
npx stylelint "**/*.scss"
```

### Git hooks

To create a pre commit hook run:
```
npx husky add .husky/pre-commit 'npm test'
```
You can edit this new file (`.husky/pre-commit`) to modify the hook.
Husky is using the available git hooks: https://git-scm.com/docs/githooks

## What if I need different settings for my project?

Please feel free to use and change all settings to fit your needs!

## Contribution

We desperately wait for your pull request!
