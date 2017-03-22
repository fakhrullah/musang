# Musang

Musang is a theme for Hugo based on [Hyde theme for Hugo](https://github.com/spf13/hyde).

I edit the theme with more configurations so this simple theme become more customizable.

<!-- ![Musang screenshot]() -->

## Contents

- [Installation](#installation)
- [Options](#options)
- [Author](#author)
- [Credits](#credits)
- [License](#license)

## Installation

1. Install this repository in the `themes/` directory:

    $ cd themes/
    $ git clone https://github.com/fakhrullah/musang.git

2. Specify `musang` as your default theme in the `config.toml` file. Just add the line

    theme = "musang"

at the top of the file.


## Options

Musang includes a lot of customizable options, typically applied via classes on the `<body>` element.

Below are variables for costumize Musang theme. All variable are optional.

```yaml

params:
  theme:
    # set menu for side bar.
    menu: main

    # sidebar options
    sidebar: 
      # sidebar stick to bottom
      # bottom | center | top
      sticky: bottom
      # sidebar position
      # left | right
      position: left

    # theme color
    # theme-color-orange | theme-color-blue | theme-color-green
    themeColor: theme-color-orange

```

### To create your own theme

1. Copy any theme-color-xxx CSS file as based, which located at `musang/static/theme-color-xxx.css` to your website `static` directory into name you wish.

```console
$ cp hugoWebDir/themes/musang/static/css/theme-color-orange.css hugoWebDir/static/css/theme-my-custom.css
$
```

2. Then, in config set `themeColor` variable under `params` > `theme` to the filename of your new created css.

```yaml
params:
  theme: 
    themeColor: theme-my-custom
```

## Author
**Fakhrullah Padzil**
- <https://github.com/fakhrullah>
- <https://twitter.com/fakhrullah>

## Credits

- [Mark Otto](https://github.com/mdo) - Original creator Hyde theme for Jekyll static site generator
- [Steven Francia](https://github.com/spf13) - for creating Hugo and porting Hyde theme
- To all Hugo static site generators contributors

## License

Open sourced under the [MIT license](LICENSE.md).
