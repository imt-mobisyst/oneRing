# HackaMove

An HackaGames game based on the multi-paths planning problem.


## Install:

_mb6-space_ can be cloned and configured accordingly to ROS2.
Also, the proposed command tools rely on a [toml](https://toml.io) based configuration file.

```sh
pip install toml toml-cli
git clone https://github.com/imt-mobisyst/mb6-space.git
cd mb6-space
./bin/set-mb6-bashrc
source ~/.bashrc
```

The `set-mb6-bashrc` script adds lines into your `~/.bashrc` file to source `./bin/run-commands.bash` automatically in your shells.


## Get Stated:

_mb6-space_ is a meta-package mainly including the documentation and some useful command tools.
It is designed to be your ros-workspace.

Connect to the [imt-mobisyst](https://imt-mobisyst.github.io/mb6-space) web pages for more information.


## Documentation

The documentation is on [Markdown](https://en.wikipedia.org/wiki/Markdown) format starting by `index.md` in the `docs` directory.
It can be served as a _HTML_ web site thanks to [MkDocs](https://www.mkdocs.org/).

```sh
mkdocs serve
```

You can then refer to the [http://127.0.0.1:8000/](documentation).
The navigation structure is defined on the `mkdocs.yml` file.

## Contribute 

Doc. deployment is achieved with a public github repository (_imt-mobisyst.github.io.git_), by copying the _mkdocs_ generated site in the `lct-pls` directory of this public repository.

```sh
mkdocs build
git clone git@github.com:imt-mobisyst/imt-mobisyst.github.io.git ../imt-mobisyst-site
rm -fr ../imt-mobisyst-site/lct-pls
mv ./site ../imt-mobisyst-site/lct-pls
git -C ../imt-mobisyst-site commit -am "lct-pls updates"
git -C ../imt-mobisyst-site push
```

For convenience, this manipulation is automatized with the script `./bin/docs-deploy.sh`.
To notice that the documentation repository can be cloned anywhere on your computer while your `config.toml` is updated accordingly.


## Some Tools

### Slide Presentations

The presentation/slides are prepared using `marp` (an extantion to Markdown permiting to generate slides pdf).
`marp` is fully integrated to VisualCode:

- Get *Marp for VS Code* extention
- On `VS Code parameters > working space > Marp for VS Code` you can add elements on `Markdown › Marp: Themes` : `style/slides.css`.
- Also authorise html tag. activate `marp: Enable HTML` in settings.

### Overleaf Web-Editor

[Overleaf](https://www.overleaf.com) is a Latex dedicated web-editor.

It is possible to clone locally overleaf project based on `git` tool.
For instance to clone a `PROJECT-NAME` from the overleaf code `CODE` : 

```bash
git clone https://git@git.overleaf.com/$CODE $PROJECT-NAME
```

by convention, the project name is built as `PROJECT-NAME= ovl-$Author$YEAR-$PROJECT`


CODE                     | Author   | PROJECT               | DATE      |
-------------------------|----------|-----------------------|-----------|
6661a9f3e44db0c19fde4c5b | Naury    | SAC                   | 2025      |
67c85987f374a5ffcce204ab | Ltaif    | DCIA                  | 2025      |
6797af19d58c0412ab4da125 | Gouget   | IROS                  | 2025      |
67ed28f0d11dfd6972fa3e09 | Alie     | PAIS                  | 2025      |


## New on Git

- **Git** is a decentralized solution for version management. Its first feature is to allow several contributors to work on a same directory, each one on its own machine.
It permits to share an entire historic of all modifications through a common *repository* on a server, to facilitate fusion of document version (mainly by using text format), and to do it in a safe way.

- A **GitServer**, *Bitbucket*, *GitHub*, [framagit](https://framagit.org) or a private install of gitlab (*[gvipers](gvipers.imt-lille-douai.fr)* at IMT Nord-Europe), propose solutions based on *git* to share a repository in the cloud with management services (groups, members, access rules).

- **Markdown Documents** is a text format, very simple and directly interpretable on all _git_ server solutions. The format follows the philosophy: **What you see is what you get**

- Going further with Git:
    * [Learn Git](https://try.github.io/)
    * [GitForWindows](https://gitforwindows.org/) a simple IDE for Windows.
    * [Learn Markdown](https://bitbucket.org/tutorials/markdowndemo)

