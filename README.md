# Test Details
## .github/workflows/push.yml
```YAML
name: Bump Version (Default="Minor")
'on':
  push: null
jobs:
  bump-version:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - id: version-bump
        uses: ./action
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
        with:
          default: minor
          patch-wording: patch

```
## Message
patch
## Starting Version
17.0.0
## Expectation
- **Version:** 17.0.1