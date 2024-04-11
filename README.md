[En Esperanto](https://github.com/Dok8tavo/senlima-chielo/blob/main/LEGUMIN.md)

# Senlima-chielo

"Senlima-chielo" (/senlima t̠ʃielo/) is a plugin for the game [Endless-sky](https://endless-sky.github.io). It replaces the original content with an esperanto translation.

## How to play Senlima-chielo

1. Get the game [Endless-sky](https://github.com/Dok8tavo/senlima-chielo/blob/main/README.md#how-to-get-endless-sky),
2. Start the game at least once,
3. Download Senlima-chielo into your plugin directory.

The plugin directory should be located depending on your operating system:

- for Linux either:
    - at `/usr/share/games/endless-sky/plugins/`, or
    - at `~/.local/share/endless-sky/plugins/`,
- for Windows either:
    - at `\plugins` in the same directory as the Endless-sky executable, or
    - at `C:\Users\yourusername\AppData\Roaming\endless-sky\plugins\`,
- for MacOS either:
    - at `Contents/Resources/plugins/` in the application bundle, or
    - at `~/Library/Application Support/endless-sky/plugins/`.

The directory that should contain the "Senlima-chielo" plugin is the one named `plugins`.

After this, whenever you make a new pilot, you can select the intro "Senlima-chielo" instead of "Endless-sky" and this pilot will use the plugin.

## How to get Endless-sky

You can get it on [steam](https://store.steampowered.com/app/404410/Endless_Sky/).

You can get it from a package manager such as `apt` on Linux.

Or you can install it [manually](https://github.com/endless-sky/endless-sky/releases/tag/v0.10.6):

## How to contribute

If your familiar with git and github, you can fork this repository and make a pull request with your changes.

If not, you can offer your translations in [the discord group](https://discord.gg/EwAKV6Yme4).

### Translation

There are three types of translation units:

- paragraph,
- proper nouns,
- common nouns,

#### Paragraphs

Paragraphs are just paragraphs of text. They can be the description of a planet or a mission, a part of a dialog, etc. Each paragraph is a separate translation unit. They can be:

- `description` blocks,
- `spaceport` blocks,
- root `phrase` blocks,
- `conversation` paragraphs,


#### Proper nouns

Proper nouns usually have a meaning for the code, they're not just text. For example the name of a fleet, a ship, a planet, a government, a system, or a mission, etc. As the code use them to designate actual content, changing one instance of a proper noun without updating the others will break the code.

That's why all the instance of a proper noun are part of only one translation unit. They all must be changed at once. That's why you should `grep -Rinw "data/" -e thepropernoun`, sure that every instance of it is commented out and is followed by its proper translation, before submitting making your commit.

#### Common nouns

Common nouns don't have any meaning for the code, but they're not just text. They have multiple instances throughout the content, but changing one without the others doesn't break the code. They're basically only a convention that must be followed when translating paragraphs and eventually proper nouns.

#### Examples

```endless-sky
# "Esperantujo" is a proper noun
planet Esperantujo
    # This is a description block:
    description "Tiu planedo estas pacema al chiuj popoloj."
    # This is another description block:
    description "Tio estas tre plaĉa loko!"
    # "kosmostacio" is a common name!
    # This is a spaceport block:
    spaceport "Tio estas priskribo de la kosmostacio."

# "conversation name" is a proper name!
conversation "conversation name"
    scene "scene/path"
    # This is a conversation paragraph:
    `Hello world!`
    # This is another conversation paragraph:
    `Goodbye world!`

# "Tradukisto" is a proper name!
person "Tradukisto"
    phrase
        `Mi estas tradukisto por Senlima-chielo!`
```