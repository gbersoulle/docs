# MKDocs

## What's MKdocs ?

MKdocs is a simple python wrapper that can convert the Markdown files (.md) into a basic static website.
It's very often used for hosting in a more visual way the documentation about something.

For now, i'm using it to self-host a basic documentation.

## How to install it.

### Installing PIP
If you're using a recent version of Python, the Python package manager, pip, is most likely installed by default. However, you may need to upgrade pip to the lasted version:
```bash
pip install --upgrade pip
```
If you need to install pip for the first time, download (get-pip.py)[!https://bootstrap.pypa.io/get-pip.py]. Then run the following command to install it:

```bash
python get-pip.py
```

### Installing MkDocs

Install the mkdocs package using pip:

```bash
pipx install mkdocs
```

You should now have the mkdocs command installed on your system. Run mkdocs --version to check that everything worked okay.

```bash
mkdocs --version
mkdocs, version 1.2.0 from /usr/local/lib/python3.8/site-packages/mkdocs (Python 3.8)
```

## How to use it ?

to use mkdocs you will need a basic structure

```bash
.
├── docs
│   └── index.md
└── mkdocs.yml
```

the basic content of the mkdocs.yml is : 

```yaml
# yaml-language-server: $schema=https://squidfunk.github.io/mkdocs-material/schema.json
site_name: Tech Docs
nav:
  - Home: index.md
```

you can now deploy your mkdocs on a web interface with

```bash
mkdocs serve
```

```bash
firefox http://localhost:8000
```
