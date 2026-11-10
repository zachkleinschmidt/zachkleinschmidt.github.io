# GodRecall

Static site for [GodRecall](https://twitch.tv/godrecall) (Zach), a Las Vegas Twitch Affiliate. GitHub Pages serves this repository from the `main` branch root. There is no build step.

## Preview

```bash
python3 -m http.server 8080
```

Then open `http://127.0.0.1:8080`. The Twitch player is included for `zachkleinschmidt.github.io`, `godrecall.com`, and `www.godrecall.com`. Anywhere else, the page shows a link to Twitch instead of a broken embed.

## Pages

- `/` — streamer hub
- `/terms-of-service.html` and `/terms/` — Recall Bot terms of service
- `/privacy-policy.html` and `/privacy/` — Recall Bot privacy policy

The font in `fonts/` is [Outfit](https://github.com/Outfitio/Outfit-Fonts), used under the SIL Open Font License (`fonts/OFL.txt`).

## Custom domain

The public site is [https://godrecall.com](https://godrecall.com). The root `CNAME` file contains `godrecall.com`. DNS:

- Apex `godrecall.com`: A records `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
- Apex `godrecall.com`: AAAA records `2606:50c0:8000::153`, `2606:50c0:8001::153`, `2606:50c0:8002::153`, `2606:50c0:8003::153`
- `www.godrecall.com`: CNAME to `zachkleinschmidt.github.io`

GitHub Pages redirects between the apex domain and `www`. Canonical and Open Graph URLs use `https://godrecall.com`.
