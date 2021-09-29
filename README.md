# Test Details
## .github/workflows/push.yml
```YAML
name: Do Nothing
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
          push: false

```
## Message
no keywords
## Starting Version
11.0.0
## Expectation
- **Version:** 11.0.0