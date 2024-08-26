# Lice2

Lice generates license files. No more hunting down licenses from other projects.

!!! note
    This project is forked from the original
    [lice](https://github.com/licenses/lice){:target="_blank"} project which
    seems to have been abandoned and is not compatible with Python 3.12.

    I have created a new project rather than issue a PR because the changes are
    quite large, and no-one is merging PR's on the original project. Otherwise,
    the Git history is preserved from the original.

This version fixes the compatibility issue with Python 3.12, and adds some new
features:

- It now uses [Poetry](https://python-poetry.org/){:target="_blank"} for
  dependency management
- Can read from a config file for default values
- Converted from 'argparse' to 'Typer' for CLI handling
- Fixes the issue where extra spaces and newlines were added to the generated
  license text. This was considered a bug by at least several users, so it was
  fixed in version `0.10.0`. However, if you want to generate a license with the
  old style, you can use the `--legacy` option or set the `legacy` key in the
  configuration file to `true`
- The code has been modernized and cleaned up, all type-hinting has been
added
- It passes strict linting with the latest 'Ruff' and 'mypy'
- GitHub actions set up for linting, `Dependabot` and `Dependency Review`

In addition, future plans can be seen in the [Future Plans](future_plans.md)
page.

!!! warning "Python Compatibility"
    This appllication is now only compatible with Python 3.9 and above. If you
    wish to use an older version, use the original 'lice' package.

    However, I'ts the **development** dependencies that are causing the
    incompatibility, so I'll look at reducing the **Production** version in
    future releases while still requiring Python 3.9 or above for development.