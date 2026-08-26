# tijdafstand — integriteitsmanifest

Hier staan de SHA-256-hashes van elk bestand dat https://www.tijdafstand.nl aan
bezoekers uitlevert. Meer niet: geen broncode, geen kaartdata.

**Waarom apart.** De app controleert of de code die je browser geladen heeft nog
klopt met wat hier staat. Zou die lijst van tijdafstand.nl zelf komen, dan
controleert de server zichzelf en bewijst het niets. Deze repo is openbaar en
niet vanaf die webserver te wijzigen.

## Zelf controleren

```sh
curl -sO https://raw.githubusercontent.com/Alseenrodelap/tijdafstand-public/main/integriteit.sha256
curl -sO https://www.tijdafstand.nl/assets/js/app.js
shasum -a256 -c integriteit.sha256 --ignore-missing
```

Het volledige gereedschap en de uitleg staan in de codebasis:
`tools/controleer.sh` en `docs/INTEGRITEIT.md`.

## Wat dit wel en niet bewijst

Het bewijst dat de bestanden die je ophaalt gelijk zijn aan wat hier gepubliceerd
is. Het bewijst **niet** dat die bestanden veilig zijn: wie zowel de webserver
als deze repo beheerst, kan beide aanpassen. Wat het wel doet is een wijziging
zichtbaar maken voor iedereen die kijkt — en dat is precies waar zo'n lijst voor
is. De volledige afweging staat in `docs/DREIGINGSMODEL.md`.

---
build `20260825T2211Z-f6c9c340` · appHash `a55519d0a669b11ba7985f7b45489019dc067991a2fe32e444001e29130f3ae4`
