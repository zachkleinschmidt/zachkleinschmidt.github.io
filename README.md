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

`godrecall.com` is not connected yet, so this repo has no `CNAME` file. When DNS is ready, add `godrecall.com` in the repository Pages settings (that writes the `CNAME`) and point DNS at GitHub Pages:

- Apex `godrecall.com`: A records `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
- Apex `godrecall.com`: AAAA records `2606:50c0:8000::153`, `2606:50c0:8001::153`, `2606:50c0:8002::153`, `2606:50c0:8003::153`
- `www.godrecall.com`: CNAME to `zachkleinschmidt.github.io`

Remove any default records the DNS host adds, and do not use a wildcard record. After both names resolve, GitHub Pages redirects between the apex domain and `www`. Confirm the IP addresses in [GitHub’s custom domain docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site) before changing DNS. Update the canonical and Open Graph URLs in the HTML if the public site URL changes.
