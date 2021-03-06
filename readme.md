Prettier does only focus on formatting rules like `comma-style` and does nothing to help with code-quality.
`eslint-config-silence` does not regulate code style rules, but focuses on:

* Prevent possible errors (e.g. `no-cond-assign`, `no-unreachable`)

* Recommends best practices (e.g. `no-eval`, `no-extend-native`)

* Code Smell Detection (e.g. `no-duplicated-branches`, `no-identical-functions`)

* Forces the use of ES6+ features (e.g. `no-var`, `prefer-const`, `prefer-spread`)

* Warnings you that complexity of the code is exceeded:
```json
"complexity": ["warn", 20],
"max-depth": ["warn", 4],
"max-lines": ["warn", 300],
"max-params": ["warn", 3],
```

## Usage
```bash
npm install -D eslint-config-silence
```

Add this to your .eslintrc file:
```json
{
  "extends": ["eslint-config-silence"]
}
```

*Note: You can also omit the `eslint-config-`*

### React
For React projects you can also use additional config:
```json
{
  "extends": ["silence/react"]
}
```

This config includes [rules of Hooks](https://reactjs.org/docs/hooks-rules.html) and recommended [accessibility rules](https://github.com/evcohen/eslint-plugin-jsx-a11y) on JSX elements.
