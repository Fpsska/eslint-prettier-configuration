
1) Add ESLint, Prettier extensions
2) Install all necessary npm packages
3) Create, configurate `.prettierrc`, `.eslintrc` files
4) Configurate IDE settings (on `formatOnSave` / `formatOnPaste` / `codeActionOnSave`)
5) Add scripts in `package.json` file


### `Preview` _.eslintrc_

```json
{
    "env": {
        "browser": true,
        "es2021": true
    },
    "extends": [
        "eslint:recommended",
        "plugin:react/recommended",
        "plugin:@typescript-eslint/recommended",
        "plugin:import/errors",
        "plugin:import/warnings",
        "plugin:import/typescript",
        "prettier"
    ],
    "plugins": [
        "@typescript-eslint",
        "import",
        "react",
        "react-hooks",
        "prettier"
    ],
    "parser": "@typescript-eslint/parser",
    "parserOptions": {
        "ecmaVersion": "latest",
        "sourceType": "module"
    },
    "rules": {
        "prettier/prettier": "error",
        "no-console": "warn",
        "quotes": ["error", "single"],
        "jsx-quotes": ["error", "prefer-double"],
        "no-unused-vars": "warn",
        "prefer-const": "error",
        "comma-dangle": ["warn", "never"],
        "semi": ["warn", "always"],
        "@typescript-eslint/no-explicit-any": "off",
        "import/order": [
            "error",
            {
                "groups": [
                    "builtin",
                    "external",
                    "internal",
                    "parent",
                    "sibling",
                    "index",
                    "object",
                    "type"
                ],
                "newlines-between": "always-and-inside-groups"
            }
        ],
        "react-hooks/exhaustive-deps": "warn"
    }
}


```

### `Preview` _.prettierrc_

```json
{
    "tabWidth": 4,
    "arrowParens": "avoid",
    "semi": true,
    "trailingComma": "none",
    "singleQuote": true,
    "jsxSingleQuote": false,
    "singleAttributePerLine": true
}
```

### `Preview` _devDependencies_
``` json
  "devDependencies": {
    "@typescript-eslint/eslint-plugin": "^5.42.0",
    "@typescript-eslint/parser": "^5.42.0",
    "eslint": "^8.26.0",
    "eslint-config-prettier": "^8.5.0",
    "eslint-plugin-prettier": "^4.2.1",
    "eslint-plugin-react": "^7.31.10",
    "eslint-plugin-react-hooks": "^4.6.0",
    "prettier": "^2.7.1"
  }
```

### `Preview` _settings.json_
``` json
  "editor.formatOnSave": true,
  "editor.formatOnPaste": true,
  "editor.codeActionsOnSave": {
    "source.fixAll": true
  },
```
## Available Scripts

```json
"scripts": {
  "lint": "eslint -c .eslintrc --ext .js,.jsx,.ts,.tsx .",
  "lint:fix": "npm run lint -- --fix"
}
```

### `Usage`

```sh
npm run lint
```
```sh
npm run lint:fix
```


