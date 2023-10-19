# React + TypeScript + Vite

## Expanding the ESLint configuration

If you are developing a production application, we recommend updating the configuration to enable type aware lint rules:

- Configure the top-level `parserOptions` property in `.eslintrc.cjs`:

```js
parserOptions: {
ecmaVersion: 'latest',
sourceType: 'module',
project: ['./tsconfig.json', './tsconfig.node.json'],
sconfigRootDir: __dirname,
},
```

- Replace `plugin:@typescript-eslint/recommended` to `plugin:@typescript-eslint/recommended-type-checked` or `plugin:@typescript-eslint/strict-type-checked`

- Optionally add `plugin:@typescript-eslint/stylistic-type-checked`

- Install [eslint-plugin-react](https://github.com/jsx-eslint/eslint-plugin-react) and add `plugin:react/recommended` & `plugin:react/jsx-runtime` to the `extends` list.

- Install [eslint-plugin-jsx-a11y](https://github.com/jsx-eslint/eslint-plugin-jsx-a11y) and add `plugin:jsx-a11y/recommended` to the `extends` list.

- Install [eslint-plugin-promise](https://github.com/eslint-community/eslint-plugin-promise) and add `plugin:promise/recommended` to the `extends` list.

- Install [eslint-plugin-sonarjs](https://github.com/SonarSource/eslint-plugin-sonarjs) and add `sonarjs` to the `plugins` option of your `.eslintrc` and/?or add `plugin:sonarjs/recommended` to the extends option to enable all recommended rules.

```js
  ...
  extends: [
    'eslint:recommended',
    'plugin:react/recommended',
    'plugin:react/jsx-runtime',
    'plugin:react-hooks/recommended',
    'plugin:jsx-a11y/recommended',
    'plugin:promise/recommended',
    'plugin:sonarjs/recommended',
    'plugin:@typescript-eslint/recommended-type-checked',
    'plugin:@typescript-eslint/stylistic-type-checked',
  ],
  ...
  plugins: ['react-refresh', 'sonarjs'],
```

## Prettier

Install Prettier locally: `yarn add --dev --exact prettier`
