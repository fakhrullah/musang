# Musang

Musang is a theme based on [Hyde theme for Hugo](https://github.com/spf13/hyde).

I edit the theme with more configurations so this simple theme become more customizable.

<!-- ![Musang screenshot]() -->

## Credits

- xxx - Original creator Hyde theme for Jekyll static site generator
- Steven Francia - for creating Hugo and porting Hyde theme
- To all Hugo static site generators contributors

## Contents

- [Installation](#installation)
- [Options](#options)
  - [Sidebar menu](#sidebar-menu)
  - [Sticky sidebar content](#sticky-sidebar-content)
  - [Themes](#themes)
  - [Reverse layout](#reverse-layout)
  - [Disqus](#disqus)
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


### Sidebar menu

Create a list of nav links in the sidebar by assigning "menu=main" in the front matter.


### Sticky sidebar content

By default Musang ships with a sidebar that affixes it's content to the bottom of the sidebar. You can optionally disabled this by removing the `.sidebar-sticky` class from the sidebar's `.container`. Sidebar content will then normally flow from top to bottom.

```html
<!-- Default sidebar -->
<div class="sidebar">
  <div class="container sidebar-sticky">
    ...
  </div>
</div>

<!-- Modified sidebar -->
<div class="sidebar">
  <div class="container">
    ...
  </div>
</div>
```


### Themes

Musang ships with 12 optional color themes. Apply a theme to change the color scheme (mostly applies to sidebar and links).

<! -- 
![Musang in orange screenshot]()
![Musang in green screenshot]()
-->

There are 12 color themes available at this time.

<!--
!Musang theme classes]()
-->

To use a color theme, add the `themeColor` variable under `params`, like so:

**TOML**
```toml
theme = "musang"

[params]
  themeColor = "theme-color-orange"
```

**YAML**
```yaml
theme: "musang"

params:
  themeColor: "theme-color-orange"
```

To create your own theme, copy any theme-color CSS file as based, which located at `musang/static/theme-color-orange.css`. Rename the file as you wish (e.g:`theme-better-orange`). Edit the file as you wish. Then change config `themeColor` params. 

### Change sidebar to right

Default sidebar is on left. To make the sidebar on right and content on left, simply add `sidebar` variable under `params` and set it to right.

<!--
![Musang with reverse layout]()
-->

**TOML**
```toml
theme = "musang"

[params]
  sidebar = right
```

### Disqus

You can optionally enable a comment system powered by Disqus for the posts. Simply add the variable `disqusShortname` to the `params` in your config file.

**YAML**
```yaml
disqusShortname: "spf13"
```

## Author
**Fakhrullah Padzil**
- <https://github.com/fakhrullah>
- <https://twitter.com/fakhrullah>

## License

Open sourced under the [MIT license](LICENSE.md).

