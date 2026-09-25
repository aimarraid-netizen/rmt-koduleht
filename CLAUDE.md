# RMT Konsult koduleht (rmtkonsult.ee)

> Kolitud koondmälust 08.09.2026. Uuenda siin, mitte mälus.

RMT Konsult OÜ kodulehe projekt (alustatud 30.08.2026).

- **LIVE-deploy** (30.08.2026): valitud v14 (teekonnarada, kaks haru; türkiis haru ALL — üleval-varianti v15 prooviti ja Aimar lükkas tagasi; "praegu"-joon jäi sisse). OG-jagamiskaart `og.png` (PIL-skript, logo PNG taust on baked #111111) + og/twitter/canonical tagid. Galerii v14 = live index.html koopia (hoia sünkis!) → public repo `aimarraid-netizen/rmt-koduleht` (`~/projects/rmt-koduleht/`, index.html + logo/; koodi hoidla), domeen **rmtkonsult.ee** (ostetud Teliast, DNS Telia iseteeninduses).
- **Serveerib rmt-web (Hetzner, Caddy) alates 25.09.2026**: DNS apex A → 2.29.10.251, www CNAME → rmtkonsult.ee, Let's Encrypt. GitHub Pages välja lülitatud (repos olev `CNAME`-fail on jääk). **Uus sisu live'i:** commit siin → `cd ~/projects/rmt-web && bin/release rmtkonsult` → `bin/check --tags apps` → `bin/apply --tags apps` (Claude pärast Aimari "jah"-i). `git push` üksi enam live'i ei vii. Eelvaade: https://rmtkonsult.2-29-10-251.sslip.io/. Kontaktid lehel: aimar@ (IT, sinine) + ragne@ (puhastus, türkiis).

- 15 landing-page versiooni (v01–v15): `~/projects/dashboard/html/rmt-koduleht/` → vaadatavad `:8080/rmt-koduleht/` (index.html = thumbnail-galerii). Aimar valib, millistega edasi töötada. Tekstipiirang: lehel ainult "RMT Konsult OÜ" + "aimar@rmtkonsult.ee", kõik muu vihjeliste fragmentidena.
- v11 = Aimari enda valitud bitmap-suund (ekraanipildilt), päises päris logo.
- **Logosüsteem "No. 91b"** (kehtiv, 30.08.2026; asendas No. 91): originaal `~/Downloads/RMT logo/`, püsikoopia `~/projects/rmt-koduleht/logo/`. Kiri IBM Plex Sans 600; ribad jämedad, kõik mõõdud ühikust 0,22em; viewBox 745×174. Värvid: #1E4FA8 IT (tumedal #4C82E0) / #3CC5C3 puhastus / #111111 tekst (tumedal #FFF). Variandid: hele-taust, tume-taust, *-plaat (taust sees), mono-hele/tume + 4× PNG-d. Min laius 90 px. NB: SVG-des kiri `<text>` elemendina → font PEAB lehel laetud olema; trükikoja jaoks outline'ida. 30.08 lisatud kõigile SVG-dele `textLength="745" lengthAdjust="spacingAndGlyphs"` — muidu ei veni kiri brauseris ribade laiuseks (disaineri tööriist venitas, brauser mitte). v11 kasutab 91b hele-taust varianti inline'ituna.
- **Logod avalikult** (25.09.2026): kõik 25 faili (lisandusid tihe, läbipaistvad PNG-d, profiil, hele-taust-kitsas) → `https://rmtkonsult.ee/logo/<fail>`. Väljaspool meie lehte kasuta PNG-d (SVG `<text>` ei saa fonti). Tihe- ja profiil-SVG-del puudub `textLength`-parandus. `.gitattributes` export-ignore hoiab CLAUDE.md ja CNAME serverist eemal (git archive).
- Ettevõttel on kaks haru: IT ja puhastusteenus. Aimar eelistas logovarianti, kus mõlemad ribad on värvilised (esindab tervet ettevõtet, mitte ainult IT-poolt).

Vt `~/projects/dashboard/CLAUDE.md` (serveerimine).

