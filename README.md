# auro-templates

This repository serves as a template for storing various configuration files, GitHub issue templates, workflows, and other configuration files.

## Contents
- **templates/**: A directory for storing various templates.
  - **default/**: A directory for storing default templates - use this when synchronizing most auro components.
    - **.github/**: A directory for storing GitHub templates. This exactly matches a "real" `.github` directory in structure
    to make copying easier.

## Usage
This template repository is primarily consumed by the `auro-cli` tool using `auro sync`. Please check out the link below for more information on how to use the `auro-cli` tool.

Secondarily, each auro component will be updated to use this repository instead of `WC-Generator` as the source for README files.

- [auro-cli](https://github.com/AlaskaAirlines/auro-cli)