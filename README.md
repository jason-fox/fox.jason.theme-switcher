# DITA Bootstrap CSS Toggler

<a href="https://www.dita-ot.org"><img src="https://www.dita-ot.org/images/dita-ot-logo.svg" align="right" height="55"></a>

_DITA Bootstrap CSS Toggler_ is a [DITA Open Toolkit plug-in](https://www.dita-ot.org/plugins) that extends the [DITA Bootstrap](https://infotexture.github.io/dita-bootstrap/) HTML output to a switch mechanism for
the CSS

<!-- MarkdownTOC levels="2,3" -->

- [Installation](#installation)
  - [Installing DITA-OT](#installing-dita-ot)
  - [Installing the Plug-in](#installing-the-plug-in)
- [Usage](#usage)
- [License](#license)

<!-- /MarkdownTOC -->

## Installation

The _DITA Bootstrap CSS Toggler_ plug-in has been tested with [DITA-OT 4.x](http://www.dita-ot.org/download). Use the latest version for best results.

### Installing DITA-OT

1.  Download the latest distribution package from the project website at
    [dita-ot.org/download](https://www.dita-ot.org/download).
2.  Extract the contents of the package to the directory where you want to install DITA-OT.
3.  **Optional**: Add the absolute path for the `bin` directory to the _PATH_ system variable.

    This defines the necessary environment variable to run the `dita` command from the command line.

See the [DITA-OT documentation](https://www.dita-ot.org/4.0/topics/installing-client.html) for detailed installation instructions.

### Installing the Plug-in

- Run the plug-in installation commands:

```console
dita install https://github.com/jason-fox/fox.jason.extend.css/archive/master.zip
dita install https://github.com/infotexture/dita-bootstrap/archive/master.zip
dita install https://github.com/infotexture/dita-bootstrap.css-toggler/archive/master.zip
```

## Usage

To add a switch to the header menu, include a list item with a `<button>`
with a `data-bs-css-href` attribute as shown. `data-bs-css-href` holds the link to the Bootstrap CSS.


```xml
<li>
  <button
    type="button"
    class="dropdown-item d-flex align-items-center"
    data-bs-css-href="https://cdn.jsdelivr.net/npm/bootswatch@5.3.2/dist/zephyr/bootstrap.min.css"
  >
    Zephyr
  </button>
</li>
```


To run, use the `html5-bootstrap` transformation and add the `css.theme.toggle` parameter.

```console
PATH_TO_DITA_OT/bin/dita -f html5-bootstrap -o out -i PATH_TO_DITAMAP \
  --css.theme.toggle=yes
```


## License

[Apache 2.0](LICENSE) © 2023 Jason Fox
