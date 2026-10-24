## knots-dev copy of Leo Haf's Misc store

This is [Leo Haf's Misc store](https://github.com/Horizon-btc/Bitcoin-store) with one change: its Bitcoin Knots app adds the [Bitcoin Knots 29.4.3rc5 community test build](https://github.com/knots-dev/bitcoin/releases/tag/v29.4.3.knots20260508rc5) and runs it by default. That build is not an official Bitcoin Knots release. Run it on test nodes only.

The app image is built from [knots-dev/umbrel-bitcoin](https://github.com/knots-dev/umbrel-bitcoin). It ships the Guix-built binary from the knots-dev release, checked at build time against `SHA256SUMS` signed by `A47D 99B6 DB0D 715D 40C5 9A20 23AE 8A8E A7E2 4E38`. Every other app here is an unchanged copy of Leo Haf's.

### Switch your Bitcoin Knots app to the test build

1. Open the App Store, click the button with three dots next to the search box, then **Community App Stores** (on umbrelOS 2.0, then **Manage**).
2. Remove `https://github.com/Horizon-btc/Bitcoin-store` (or `https://github.com/Retropex/Bitcoin-store`, the same store).
3. Add `https://github.com/knots-dev/Bitcoin-store`.
4. Update Bitcoin Knots. Your chain data and settings stay as they are. Leave the Version tab on **Always use the latest version** to run 29.4.3rc5.

Both stores use the store ID `btc`, so add only one of them at a time. With both added, Leo Haf's app keeps priority and no update appears.

### Switch back

Remove this store, add `https://github.com/Horizon-btc/Bitcoin-store` again and update Bitcoin Knots. If you picked 29.4.3rc5 on the Version tab, the update first sets it back to **Always use the latest version**, so the app starts.

This works only for the Bitcoin Knots app from Leo Haf's store (`btc-bitcoinknots`). The Bitcoin Knots app from the Umbrel App Store cannot switch this way.
