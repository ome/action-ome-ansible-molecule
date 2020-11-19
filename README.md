# Molecule action

A GitHub action to test your [Ansible](https://www.ansible.com/) role using [Molecule](https://molecule.readthedocs.io/en/stable/).

For information on this Python package see [`README.rst`](README.rst).

## Inputs

### `scenario`

The molecule scenario to run. Default `default`

### `manage-virtualenv`

If `false` you are responsible for creating the Python environment, default `true` (this action will create a virtualenv `~/venv` and install dependencies).

## Example usage

Here is a default configuration.

```yaml
---
on:
  - push

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: checkout
        uses: actions/checkout@v2
      - name: molecule
        uses: manics/action-ome-molecule@master
```
