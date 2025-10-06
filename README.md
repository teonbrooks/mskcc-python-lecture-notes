# Intro to Scientific Python

Hello and welcome to Intro to Scientific Python!

To get started, we need to install the necessary packages.
There's a `pyproject.toml` in this folder that describes all the libraries we will be using for this class.

To install, go to your base directory of this folder and run the following command:

`pip install -e '.'`

By default, `pip`, the Python installation manager, will look for the `pyproject.toml` file and install its dependencies.

## Slide Presentation

The slides for this class are written in Markdown and presented using [Marp](https://marp.app/).

You will first need to install `marp-cli`, which is the cli tool for building html/pdf, etc. from markdown.

```bash
$ npm install --save-dev @marp-team/marp-cli
```

To build the presentation for a module, please do the following:

```bash
$ npx marp modules/module_01.md -o modules/html/module_01.html
```

You can also use VSCode for live preview of your slides. Please install the VSCode extension, [Marp for VS Code](https://marketplace.visualstudio.com/items?itemName=marp-team.marp-vscode).

## Future Consideration

- Jupyter Book support
`uv run --with jupyter jupyter book`
