# NIEHS Scientific Developers Guide

Welcome to the NIEHS Scientific Developers Guide. While some of this information is targeted at NIEHS, there are many concepts that are applicable to other ICs.

## Building

This guide is built using [Quarto](https://quarto.org). You can render it locally using `quarto render` or `quarto preview`.

To restore the R and Python environments, follow the instructions in the [Quarto Virtual Environments Guide](https://quarto.org/docs/projects/virtual-environments.html#restoring-environments)

### Restore Python {.platform-table}

To reproduce the environment on another machine you create an empty environment, activate it, and then `pip install` using `requirements.txt`:

First, follow the [using venv](https://quarto.org/docs/projects/virtual-environments.html#using-venv) for creating and activating a virtual environment for your platform/shell.

Then, install packages from `requirements.txt`:

+--------------+------------------------------------------------+
| Platform     | Command                                        |
+==============+================================================+
| Mac/Linux    | ```{.bash filename="Terminal"}                 |
|              | python3 -m pip install -r requirements.txt     |
|              | ```                                            |
+--------------+------------------------------------------------+
| Windows      | ```{.bash filename="Terminal"}                 |
|              | py -m pip install -r requirements.txt          |
|              | ```                                            |
+--------------+------------------------------------------------+

### Restore R

To [reproduce the environment on another machine](https://quarto.org/docs/projects/virtual-environments.html#restoring-environments-2) use the `renv::restore()` function:

``` r
renv::restore()
```

## Contributing

If you would like to contribute, please open an issue first so that we can discuss the changes before making them.

## Rendering

This guide is currently rendered locally before being deployed. Therefore, if your suggestion for improvemnent has been approved, then create a pull request and I will approve it, then pull and build manually before publishing.

In the future I will automate the building process.