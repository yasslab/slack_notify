# (WIP) Slack Notify for GitHub Actions

Simple [GitHub Actions](https://github.com/features/actions) to send its result to a Slack channel. :bell:

<!--![Idobata Notify examples](https://user-images.githubusercontent.com/155807/135367296-95b223db-0040-4560-8d32-20bff5c97839.png)-->

<br>

## How to use

```
# Single job use

  - name: 🔔 Notify results
    uses: yasslab/slack_notify
    if: always()
    with:
      slack_hook_url: ${{ secrets.SLACK_GITHUB_ACTIONS }}
```

<!-- TBD feature
```
# Matrix

  notify:
    needs: test # depends where the matrix job is located
    runs-on: ubuntu-latest
    if: always()
    steps:

      - name: 🔔 Notify results
        uses: yasslab/slack_notify
        with:
          slack_hook_url: ${{ secrets.SLACK_GITHUB_ACTIONS }}
          status: ${{ needs.test.result }} # passing the matrix jobs results
```
-->


## LICENSE

- [MIT License](https://github.com/yasslab/slack_notify/blob/main/LICENSE).
- Revised and inherited from [yasslab/idobata_notify](https://github.com/yasslab/idobata_notify) plugin.

<br>

## Copyright

Copyright &copy; [YassLab Inc.](https://yasslab.jp) 2023

[![YassLab 株式会社ロゴ](https://yasslab.jp/img/logos/800x200.png?cache=clear)](https://yasslab.jp/)
