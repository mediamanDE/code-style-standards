# mediaman Linting and Code Style Standards for JS and TS

This repository contains rational presets for typical JavaScript or TypeScript based projects.

It is using:

- eslint (https://eslint.org/)
- prettier (https://prettier.io/)

## Installation

### Prettier

```
npm i -D  eslint-config-prettier eslint-plugin-prettier prettier
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

## Usage

Copy these files to your project's root directory:

```
├── .eslintrc.json
└── .prettierrc.json
```

You can also find some npm script examples in the package.json that can be used as a reference.

## What if I need different settings for my project?

Please feel free to use and change all settings to fit your needs!

## Contribution

We desperately wait for your pull request!
