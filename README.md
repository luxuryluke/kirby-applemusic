# Apple Music Field Plugin for Kirby

![Plugin Preview](src/assets/plugin-preview.png)

This plugin adds an Apple Music Embed field type for Kirby including a live preview of the embed in the panel.

## Installation

### [Kirby CLI](https://github.com/getkirby/cli)
    
    kirby plugin:install scottboms/kirby-applemusic

### Git submodule

    git submodule add https://github.com/scottboms/kirby-applemusic.git site/plugins/kirby-applemusic

### Copy and Paste

1. [Download](https://github.com/scottboms/kirby-applemusic/archive/master.zip) the contents of this repository as Zip file.
2. Rename the extracted folder to `kirby-applemusic` and copy it into the `site/plugins/` directory in your Kirby project.

## Usage

### Blueprints

1. In a Page blueprint, add a new field with the type `applemusic`. Standard field attributes such as `label`, `required`, `help`, etc. can also be used to override the defaults.

```
fields:
  music:
    label: Apple Music Embed
    type: applemusic
```
2. Paste in the Music album or track id code into the field.
or
2. Paste in the embed code you copied from Music using the "Embed" share method.
or 
2. Paste in the share url link you grabbed from Music like this: `https://music.apple.com/us/album/where-is-my-mind/1165219808?i=1165219842`

(explanation about song or album IDs if necessary?)

3. Test rendering in your site in test environment?

### Templates

Based on the above example Blueprint, to render the field in your template you can use `<?= $page->music() ?>`. Note that any additional helper functions applied may break the embed. You do not need to use `->kt()` or `->kti()` for example.

## Compatibility

* Kirby 4.x
* Kirby 5.x

## Disclaimer

This plugin is provided "as is" with no guarantee. Use it at your own risk and always test before using it in a production environment. If you identify an issue, typo, etc, please [create a new issue](/issues/new) so I can investigate.

## License

[MIT](https://opensource.org/licenses/MIT)
