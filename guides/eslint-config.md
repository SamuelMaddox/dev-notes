# ESLint Config

> ⚠️ This may be changing soon. See [ESLint New Flat Configuration Files](https://eslint.org/docs/latest/use/configure/configuration-files-new). With the new flat configuration file, some config packages may have different import names. For example: [typescript-eslint](https://typescript-eslint.io/getting-started/typed-linting). This section may need updated once the new flat configuration files are more widely adopted

Projects scaffolding libraries usually include their own linting rules and configuration packages. Here are some examples of such packages:

- `eslint-plugin-react`
- `eslint-plugin-react-hooks`
- `next/core-web-vitals`
- `plugin:@angular-eslint/recommended`

Additionally we want to make sure that the following configurations are added to the project; if they're not already included as part of the above configurations:

- `eslint:recommended`
- `plugin:@typescript-eslint/recommended`
- `plugin:storybook/recommended`
- `prettier`

Finally, we want to add some custom rules for `no-console` and `no-restricted-syntax`-`TSEnumDeclaration`

The end result of all these criteria may look something like this `.eslintrc` file taken from a `NEXT.js` project:

```json
{
  //...
  "extends": [
    "eslint:recommended",
    "plugin:@typescript-eslint/recommended",
    "next/core-web-vitals",
    "plugin:storybook/recommended",
    "prettier"
  ],
  "rules": {
    "no-console": ["warn", { "allow": ["warn", "error"] }],
    "no-restricted-syntax": [
      "error",
      {
        "selector": "TSEnumDeclaration",
        "message": "Enums are forbidden. Use string union types instead. Example: type Suit = 'HEARTS' | 'DIAMONDS' | 'SPADES' | 'CLUBS';"
      }
    ]
  }
}
```
