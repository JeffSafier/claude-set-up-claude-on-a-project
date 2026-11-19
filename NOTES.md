# Notes

## Running tests

- `npm test` runs all tests with the built-in `node --test` runner (no Jest/Mocha).
- `node --test tests/users.test.js` runs a single test file.
- Add `--test-name-pattern="<regex>"` to run only matching tests.
- `npm run lint` runs ESLint. CI runs lint and then tests on Node 22 for every push and PR, so both must pass.

## Conventions

- Added use spaces not tabs and Use snake_case for variables

## Permissions

I added permissions:

```json
{
  "permissions": {
    "allow": ["Bash(npm test:*)"],
    "ask": ["Bash(git push:*)"],
    "deny": ["Read(./.env)", "Bash(git push --force:*)"]
  }
}
```
If the deny is missing than anyone can read the env file and force push the repo