# 5e Markdown

This repo helps in producing markdown versions of 5e data.  You can find markdown for the SRD on the
[Releases Page](https://github.com/scottTomaszewski/5e-markdown/releases).

#### Zips Available

On each release, there are two possible zip artifacts:

- `collapsed_sources_no_images.zip` - Just markdown, no images.  Less than 25Mb compressed 
- `collapsed_sources_with_tokens.zip` - Markdown and monster tokens, only generates when SOURCES are added.  Over 600Mb with all sources

## Usage

As is, Github Actions for this repo will only generate markdown for the SRD.  To generate markdown for content you own, start by making a (private) github repo using this repo as a template (See [Github Docs - Creating a repository from a template](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template))

![image](https://user-images.githubusercontent.com/5295276/200853381-ba0f4da4-3117-40bc-924b-8c824056baa1.png)

In your newly generated repo, 

1. Update the `config.json` file with the sources you want.  For information on how to use this file, see the json5e-convert-cli [json documentation](https://github.com/ebullient/json5e-convert-cli#additional-parameters)
    1. There are two additional fields here: `json5e_convert_cli_version` for the version of json5e-convert-cli and `version_5etools` for the version of 5etools
2. Commit and push the change
3. Wait up to 20 minutes for the cli converter to do its thing
4. When finished, go to your repo's Releases Page and download the markdown

**Backup your vault or use a test vault before using this data!**

To integrate into your obsidian vault,

1. Extract the zip to your vault 
   1. The `compendium` and `rules` folders need to be at the top-level to support links.  I'll fix this one day
3. TTRPG Statblock plugin
   1. Open the plugin settings and enable `Parse Frontmatter for Creatures` and enable the `Disable 5e SRD` to use these statblocks
   2. Set the `Beastiary Folder` to the extracted folder you dumped in your vault (`compendium` should be fine?)
   3. Might need to reload the app?  Idk... Some indexing stuff...

## Disclaimer

Okay, don't be stupid here: only download content that you own.  If you're downloading 
this data, its because you enjoy this game.  If we want to continue enjoying the game we
need to support the creators (WotC, etc) and incentivize them to continue content 
development.  Seriously, those artists, writers, etc have families too.  

This repo is for all the people who have purchased content on 1-3...4...5?? 
platforms at this point and just want it in the format they find most useful.  All I'm 
saying is that if you pull data for a source, please just go throw some cash their way,
ideally go buy at a local gaming store <3

## Attribution

This repo takes advantage of 
[json5e-convert-cli](https://github.com/ebullient/json5e-convert-cli) which is under the
Apache 2.0 license. 

This repo uses
[5etools mirror](https://github.com/5etools-mirror-1/5etools-mirror-1.github.io) as a
data source which is under the MIT license.

## License

This is MIT, do whatever you want with it <3
