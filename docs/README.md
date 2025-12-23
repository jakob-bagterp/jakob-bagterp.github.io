# Documentation Site 📚
The documentation template and build pipeline is based on [Zensical](https://zensical.org/) – a rewritten extension of [MkDocs](https://www.mkdocs.org/) and [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) – and this directory contains the source files for building the documentation.

## Configuration
Find the configuration in the `mkdocs.yml` file in the root of the project.

## Dependencies
Overview of the dependencies:

* Build tool: [Zensical](https://zensical.org/)

You can find all the dependencies in the `/docs/requirements.txt` file. How to install them from the root of the project:

```bash
pip install -r ./docs/requirements.txt
```

## Build Pipeline
All build steps and documentation testing are automated using [GitHub Actions](https://github.com/features/actions).

You can find the workflow files in the `/.github/workflows` directory. For example:

* `test_docs.yml`
* `docs.yml`

## Useful Commands
### Build
Basic build command:

```bash
zensical build
```

For more verbose output and stricter checks, use the following command:

```bash
zensical build --strict
```

### Local Development and Previewing
To preview the documentation hosted on a local machine, use the following command:

```bash
zensical serve
```

### Troubleshooting
If you're running a virtual environment with [`venv`](https://docs.python.org/3/library/venv.html) (e.g. created with the command `python3 -m venv .venv`), sometimes the dependencies break for unknown reasons.

After activating the virtual environment with the `source .venv/bin/activate` command, try using the following commands instead:

```bash
python3 -m zensical build
python3 -m zensical serve
```

Or trying executing the commands with a specific version of Python:

```bash
python3.11 -m zensical build
python3.11 -m zensical serve
```
