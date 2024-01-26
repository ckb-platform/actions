# refresh-submission Action

**NOTE**: This action assumes the backend APIs running at https://codekatabattle.fly.dev/api/v1/

## Example workflow

```yaml
on: [push]

env:
  BATTLE_ID: '<CURRENT_BATTLE_ID>'

jobs:
  refresh:
    runs-on: ubuntu-latest
    name: Refresh submission
    steps:
      - id: refresh-submission
        uses: ckb-platform/refresh-submission-action@v1
        with:
          username: "${{ secrets.USERNAME }}"
          password: "${{ secrets.PASSWORD }}"
          battle_id: "$BATTLE_ID"
          github_token: "${{ secrets.GITHUB_TOKEN }}"
```
