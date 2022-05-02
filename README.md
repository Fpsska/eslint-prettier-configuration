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
### `Preview`

```json
{
    "extends": [
        "react-app",
        "react-app/jest"
    ],
    "rules": {
        "no-console": "warn",
        "quotes": ["error", "single"],
        "jsx-quotes": ["error", "prefer-double"],
        "prefer-const" : "error",
        "comma-dangle": ["warn", "never"],
        "semi": ["warn", "always"],
        "import/order": ["error", {
            "groups": ["builtin", "external", "internal", "parent", "sibling", "index", "object", "type"],
            "newlines-between": "always-and-inside-groups"
        }]
    }
}
```



