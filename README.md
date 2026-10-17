# xray-knife-action demo

Minimal consumer repository for [zaoanshijie/xray-knife-action](https://github.com/zaoanshijie/xray-knife-action).

```yaml
- uses: zaoanshijie/xray-knife-action@v1
  id: net
  with:
    subscription: ${{ secrets.SUBSCRIPTION_URL }}
    export-env: true

- run: curl -fsS https://api.ipify.org
```

The workflow in `.github/workflows/demo.yml` starts a throw-away Xray server and a subscription that
points at it, so the demo runs without any real account. Replace that fixture with your own subscription
secret to use it for real.
