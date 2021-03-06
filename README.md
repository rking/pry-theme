![Pry Theme][logo]

* Repository: [https://github.com/kyrylo/pry-theme/][pt]
* Wiki: [https://github.com/kyrylo/pry-theme/wiki][wiki]

Description
-----------

Pry Theme is a plugin for [Pry][pry], which helps you to customize your Pry
colors via `prytheme` files.

![Railscasts](/kyrylo/pry-theme/raw/master/screenshots/railscasts.png)
![Solarized](/kyrylo/pry-theme/raw/master/screenshots/solarized.png)
![Tomorrow](/kyrylo/pry-theme/raw/master/screenshots/tomorrow.png)
![Zenburn](/kyrylo/pry-theme/raw/master/screenshots/zenburn.png)

Installation
------------

All you need is to install the gem. The `pry-theme` plugin will be detected and
used automatically.

    gem install pry-theme

Synopsis
--------

### Theme files

Theme file is a valid YAML file, which has `.prytheme` extension (for example,
`beautiful.prytheme`). In order to set up the desired theme, add the following
line into your `.pryrc`:

    Pry.config.theme = "theme-name"

The default theme is `pry-classic` (basically, you won't notice it, because
it copies the default outlook of Pry, just as you didn't install anything).
Let's change it to something more neoteric:

    Pry.config.theme = "pry-modern"

That's all! Launch your Pry and you will see the changes.

### CLI

Pry Theme has a command-line interface available via Pry. Just launch Pry and
start working with it. For example, you can _temporary_ change themes on the
fly (only for the current session):

    [1] pry(main)> pry-theme pry-classic

This will switch your current theme to `pry-classic`.

You can find [more information about CLI in Pry Theme Wiki][cli].

### Creating themes

Creating new themes isn't hard. [Check out Pry Theme Wiki article on that][new_theme].

### Adding new themes

Theme files must have `.prytheme` extension. Check out [Pry Theme Collection][ptc],
if you want to find some themes other than default ones.

* On GNU/Linux and Mac OS

    Put your theme file in `$HOME/.pry/themes` directory.

If you don't want to bother with routine operations, you can install a theme
from the Collection with help of `pry-theme -i <name>` command. For example, you
can install tomorrow-night theme: `pry-theme -i tomorrow-night`.

Oh, and don't forget to adjust your `.pryrc`!

Limitations
-----------

Basically, it will run on any terminal that is capable of displaying 256 colors,
but with a couple of admonishments. They are listed below.

### OS support

* GNU/Linux;
* Mac OS.

I hope it runs on Windows too, but I couldn't find any sane terminal, that
would support 256 colors. Sorry, Windows guys. Please, file an issue, if you
noticed bugs or something.

### Ruby implementations support

* MRI 1.9.3
* MRI 1.9.2
* MRI 1.8.7
* REE 1.8.7-2012.02
* JRuby 1.6.7
* Rubinius 1.2.4

Under the hood
--------------

Basically, Pry Theme is nothing but a CodeRay color scheme with a human-readable
syntax.

Credits
-------

* Thanks to [banister][johndogg] for bringing the plugin in masses and
  contributing a bunch of themes;
* Thanks to Karandashev for "Puzzle" font;
* Thanks to Creatica for "Dited" font;
* Thanks to [noprompt][noprompt] for a HEX to ANSI conversion Ruby
  implementation, which I borrowed from one of his projects.

License
-------

The project uses Zlib License. See LICENSE file for more information.

[pt]: https://github.com/kyrylo/pry-theme/ "Home page"
[logo]: http://img-fotki.yandex.ru/get/5107/98991937.a/0_7c6c8_871a1842_orig "Pry Theme"
[pry]: https://github.com/pry/pry/ "Pry's home page"
[new_theme]: https://github.com/kyrylo/pry-theme/wiki/Creating-a-New-Theme
[cli]: https://github.com/kyrylo/pry-theme/wiki/Pry-Theme-CLI
[wiki]: https://github.com/kyrylo/pry-theme/wiki
[ptc]: https://github.com/kyrylo/pry-theme-collection
[johndogg]: https://github.com/banister/ "John Dogg"
[noprompt]: https://github.com/noprompt/ "Joel Holdbrooks"
