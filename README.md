# The Undertomes in 5e.tools

> **Face the JSON. Save the Content.**

[![Format](https://img.shields.io/badge/format-5e.tools%20homebrew-5b3a70?style=for-the-badge)](https://5e.tools/)
[![Rules](https://img.shields.io/badge/rules-D%26D%205e%20%282014%29-8b2635?style=for-the-badge)](https://2014.5e.tools/)
[![Support](https://img.shields.io/badge/support-The%20Undertomes-f96854?style=for-the-badge)](https://www.patreon.com/cw/TheUndertomes)

![logo](https://theundertomes.crd.co/assets/images/image01.png?v=1f331208)

**The Undertomes in 5e.tools** is a curated conversion project that makes publicly available Undertomes homebrew content usable in the 2014 version of 5e.tools.

The collection is divided into three main files. The ***General Rules Compendium*** has all the general rules (from conditions to types of items). ***Project Moon*** contains subclasses and related content inspired by Project Moon works. ***Public Library*** contains all other content made by The Undertomes.
And extra files for special tomes and brews released by The Undertomes Team.

## Installation

> [!IMPORTANT]
> **General Rules must be added or the collections will not work correctly.**

### Install from a URL

1. Open [5e.tools (2014)](https://2014.5e.tools/).
2. Open **Manage Homebrew** from the site menu.
3. Choose the option to **load homebrew from a URL**.
4. Copy the URL from below and paste it in the box.
6. Refresh [5e.tools (2014)](https://2014.5e.tools/) if the newly added content does not appear immediately.

| Tome | Required | Raw JSON URL |
| --- | :---: | --- |
| **General Rules** | Yes | [Add The Undertomes: General Rules Compendium](https://raw.githubusercontent.com/twofelled/Undertomes-in-5e-tools/refs/heads/main/The%20Undertomes%3B%20General%20Rules%20Compendium.json) |
| **Project Moon** | No | [Add The Undertomes: Project Moon](https://raw.githubusercontent.com/twofelled/Undertomes-in-5e-tools/refs/heads/main/The%20Undertomes%3B%20Project%20Moon.json) |
| **Public Library** | No | [Add The Undertomes: Public Library](https://raw.githubusercontent.com/twofelled/Undertomes-in-5e-tools/refs/heads/main/The%20Undertomes%3B%20Public%20Library.json) |
| **Brewathon #1 - District 11's Travel Brochure** | No | [Add District 11's Travel Brochure](https://raw.githubusercontent.com/twofelled/Undertomes-in-5e-tools/refs/heads/main/The%20Undertomes'%20Community%3B%20District%2011's%20Travel%20Brochure.json) |


For copying:

#### General Rules
```text
https://raw.githubusercontent.com/twofelled/Undertomes-in-5e-tools/refs/heads/main/The%20Undertomes%3B%20General%20Rules%20Compendium.json
```
#### Project Moon
```text
https://raw.githubusercontent.com/twofelled/Undertomes-in-5e-tools/refs/heads/main/The%20Undertomes%3B%20Project%20Moon.json
```
#### Brewathon #1 - District 11's Travel Brochure
```text
https://raw.githubusercontent.com/twofelled/Undertomes-in-5e-tools/refs/heads/main/The%20Undertomes'%20Community%3B%20District%2011's%20Travel%20Brochure.json
```
#### Public Library
```text
https://raw.githubusercontent.com/twofelled/Undertomes-in-5e-tools/refs/heads/main/The%20Undertomes%3B%20Public%20Library.json

```

### Install from downloaded files

If loading from a URL is unavailable:

1. Open each raw JSON link above.
2. Save each file with the `.json` extension.
3. Open **Manage Homebrew** in 2014.5e.tools.
4. Upload the General Rules file.
5. Upload the Project Moon file.

## Troubleshooting

### References, conditions, or features are missing

Confirm that **both** JSON files are installed and that ***General Rules*** was loaded before ***Project Moon***. ***Project Moon*** intentionally references shared records from ***General Rules*** instead of duplicating them.

### Updated content does not appear

If you're having trouble with a new update, remove the previous version, reload the current raw URLs, and refresh the page. If necessary, perform a hard refresh. Homebrew is stored in the browser, so a different browser or browser profile may have a separate collection.

### A subclass feature fails to load

Subclass feature identifiers must agree everywhere they are referenced. Check the feature name, class name and source, subclass short name and source, and level in both `subclassFeatures` and `subclassFeature`. Report here if it isn't the case.

## Adding New Content

New brews should be added to the most appropriate existing Tome. Create a new Tome only when the content has a distinct theme or requires a separate shared ruleset.

### Project conventions

- **Preserve the original homebrew wording.** We're porting over the original wording, so any mistakes should be kept and reported to The Undertomes Team in the appropriate channels.
- Include only brews that have already been made public by The Undertomes. Respect their [Patron](https://www.patreon.com/cw/TheUndertomes)!
- Put shared systems in **General Rules**, anything that two or more brew reference should be in there.
- Put rules unique to a subclass or brew in the tome that contains that brew.
- Keep full subclass names in `name`; use `shortName` only for the shorter label shown by the subclass selector.
- Place a subclass's opening flavor text in its first-level feature wrapper before the first feature reference so it appears at the top of the class page.
- Keep classes in alphabetical order in the tomes: for example, `Barbarian`, `Cleric`, `Monk`, then `Ranger`.
- Within each class, keep subclasses in alphabetical order.
- Store Core Bursts as `optionalfeature` records under the custom Core Burst feature type.
- Do not add `page` fields.
- Use renderer tags for references to spells, conditions and rolls when appropriate.

### Suggested workflow

1. Start from the latest version of the appropriate Tome.
2. Read the entire public source and identify its content types.
3. Add or update the source metadata.
4. Transcribe the information, such as `subclass`, `subclassFeature`, `condition`, `optionalfeature`, `item`, or `variantrule`.
5. Check every internal reference, dependency, feature UID, and renderer tags. Failure to do so might cause the rendered to break.
6. Load both files in 5e.tools and test the pages.
7. Commit the updated JSON without replacing or altering unrelated public brews.
8. Create a Pull Request with said commit and it will be merged if it passes steps 5 and 6.

### Useful references

- [5e.tools Homebrew Repository](https://github.com/TheGiddyLimit/homebrew) | examples, naming conventions, installation guidance, and contribution information.
- [5e.tools Data Repository](https://github.com/5etools-mirror-3/5etools-src/tree/main/data) | official data structures to use as example.
- [5e.tools Renderer Demo](https://5e.tools/renderdemo.html) | examples of renderer entry types and inline tags.
- [5e.tools Text Converter](https://5e.tools/converter.html) | a starting point for supported stat-block conversions.
- [5e.tools Discord](https://discord.gg/5etools) | community help.
- [5etools Language Server for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=revilowaldow.5etools-language-server) | live validation and editing assistance.

## Fan Content Notice

This is an independent **fan-content conversion project**. It is **not affiliated with, endorsed by, sponsored by, or officially associated with 5e.tools or The Undertomes**.

The collection will contain **only homebrew that has been publicly released**. Inclusion in this repository does not transfer ownership of the original work. Credit and ownership remain with the respective creators.

This repository provides the conversion for personal tabletop use. Users are responsible for respecting the original creators' terms and removing content if a creator wills it so.

---
