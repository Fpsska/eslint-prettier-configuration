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
### `Preview` _.eslintrc_

```json
{
    "env": {
        "browser": true,
        "es2021": true
    },
    "extends": [
        "eslint:recommended",
        "prettier",
        "plugin:react/recommended",
        "plugin:@typescript-eslint/recommended",
        "plugin:import/errors",
        "plugin:import/warnings",
        "plugin:import/typescript"
    ],
    "plugins": ["react", "@typescript-eslint", "import"],
    "parser": "@typescript-eslint/parser",
    "parserOptions": {
        "ecmaVersion": "latest",
        "sourceType": "module"
    },
    "rules": {
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
        ]
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
	"singleAttributePerLine": true
}
```

### `Preview` _devDependencies_
``` json
  "devDependencies": {
    "@typescript-eslint/eslint-plugin": "^5.40.0",
    "@typescript-eslint/parser": "^5.40.0",
    "eslint-config-prettier": "^8.5.0",
    "eslint-plugin-react": "^7.31.10",
    "prettier": "^2.7.1",
    "eslint": "^8.25.0"
  }
```
1) Add ESLint, Prettier extensions
2) Set Prettier as default formatter
3) Enable on save formatting
