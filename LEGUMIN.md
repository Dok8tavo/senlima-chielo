[In English](https://github.com/Dok8tavo/senlima-chielo/blob/main/README.md)

# Senlima-chielo

"Senlima-chielo" estas aldono por la ludo [Endless-sky](https://endless-sky.github.io). Ĝi provizas esperante tradukita versio de la originala enhavo.

## Kiel ludi je Senlima-chielo

1. Ekhavu la ludon [Endless-sky](https://github.com/Dok8tavo/senlima-chielo/blob/main/LEGUMIN.md#l29),
2. Ŝaltu la ludon almenaŭ unufoje,
3. Metu Senlima-chielo en la aldondosierujon.

La aldondosierujo troviĝu laŭ via operaciumo:

- por Linukso aŭ:
    - ĉe `/usr/share/games/endless-sky/plugins/`, ău
    - ĉe `~/.local/share/endless-sky/plugins/`,
- por Vindozo ău:
    - ĉe `\plugins` en la sama dosiero kiel Endless-sky, aŭ
    - ĉe `C:\Users\{your username}\AppData\Roaming\endless-sky\plugins\`,
- por Makintoŝo aŭ:
    - ĉe `Contents/Resources/plugins/` en la apujo, aŭ
    - ĉe `~/Library/Application Support/endless-sky/plugins/`.

La dosierujo kiu enhavu la "Senlima-chielo" aldono nomiĝas `plugins`.

Poste, ĉiam kiam vi kreas novan piloton, vi elektu la komencon "Senlima-chielo" anstataŭ "Endless-sky", por uzi la aldonon.

## Kiel ekhavi Endless-sky

Vi povas preni ĝin per [steam](https://store.steampowered.com/app/404410/Endless_Sky/).

Vi povas preni ĝin per "package manager" kiel `apt` ĉe Linukso.

Aŭ vi povas preni ĝin [per vi mem](https://github.com/endless-sky/endless-sky/releases/tag/0.10.6).

## Traduko

There are three types of translation units:
Estas tri tipoj de tradukero.

- paragrafoj,
- propraj nomoj,
- oftaj nomoj.

### Paragrafoj

Paragrafoj simple estas tekstopartoj. Ili povas esti priskribo de planedo, de misio, parto de dialogo, ktp. Ĉiu paragrafo estas aparta tradukero. Ili povas esti:

- `description` (priskribaj) blokoj,
- `spaceport` (kosmostaciaj) blokoj,
- radikaj `phrase` (frazaj) blokoj,
- `conversation` (interparolaj) paragrafoj,

### Propraj nomoj

Propraj nomoj kutime havas sencon kode, ili ne estas simplaj tekstoj. Ekzemple, namo de ŝiparo, ŝipo, planedo, popolo, sistemo, aŭ misio, ktp. Pro tio ke proprajn nomojn la kodo uzas por dezigni enhavon, ŝanĝi unu okazon de propra nomo dum ne ŝanĝi la aliaj kaŭzas problemojn al la kodon.

Tial ĉiuj okazoj de propra nomo estas parto de la sama tradukero. Ili ĉiuj estu ŝanĝata samtempe. Tial oni faru `grep -Rinw "data/" -e propranomo`, por certiĝi ke ĉiu okazo estu forkomentita kaj sekvita de ĝia traduko.

### Komunaj nomoj

Komunaj nomoj ne havas sencon kode, sed ili ne estas simple teksto. Estas multaj okazoj da ili en la enhavo, sed ŝanĝi nur unu ne kaŭzas problemojn al la kodon. Ili nur estas konsento kiun oni sekvu kiam oni tradukas paragrafojn.

### Ekzemploj

```endless-sky
# "Esperantujo" estas propra nomo
planet Esperantujo
    # Tio estas priskriba bloko:
    description "Tiu planedo estas pacema al chiuj popoloj."
    # Tio estas alia priskriba bloko:
    description "Tio estas tre plaĉa loko!"
    # "kosmostacio" estas komuna nomo!
    # Tio estas kosmostacia bloko:
    spaceport "Tio estas priskribo de la kosmostacio."

# "conversation name" estas propra nomo!
conversation "conversation name"
    scene "scene/path"
    # Tio estas interparola paragrafo:
    `Hello world!`
    # Tio estas interparola paragrafo:
    `Goodbye world!`

# "Tradukisto" estas propra nomo!
person "Tradukisto"
    phrase
        `Mi estas tradukisto por Senlima-chielo!`
```

## Kiel kunlabori

Se vi konas la funkcion de "git" kaj "github" vi povas _forki_ ĉi tiun deponejon kaj peti altiron kun viaj ŝanĝoj.

Alie vi povas proponi viajn tradukojn de [la diskorda grupo](https://discord.gg/EwAKV6Yme4).

