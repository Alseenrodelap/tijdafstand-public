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
curl -sO https://www.tijdafstand.nl/app/assets/js/app.js
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
build `20260827T2201Z-420e4f95` · appHash `9b415292eeb3a1a6117ca3f38a99c9e541ec34ad5bbdd4e501c1ff913574d6a7`
