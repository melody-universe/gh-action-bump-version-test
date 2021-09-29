# Test Details
## .github/workflows/push.yml
```YAML
name: Bump Version
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

```
## Message
major
## Starting Version
6.0.0
## Expectation
- **Version:** 7.0.0