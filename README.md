# auro-templates

The source of truth for what lives in every Auro component repo's `.github/` folder and its README. auro-cli pulls from here with `auro sync`.

## What's in here

```
templates/
  default/        use this for most components
    .github/      matches a real .github folder exactly: workflows, issue and PR templates, CODEOWNERS
    partials/     reusable markdown chunks (browser support, install, usage) that build the README
    README.md     the README template for components
    index.md      the docs landing page template
    api.md        the component API doc template
  formkit/        a variant for formkit
```

The `.github/` folder here matches a real one exactly, so copying is a straight mapping. The caller workflows in `default/.github/workflows/` are what invoke auro-actions in each component repo.

## How it's used

The main consumer is auro-cli:

```bash
auro sync
```

`auro sync` reads `templates/default/.github/` from this repo over the GitHub API, then rewrites the component's local `.github/` to match. Each component repo also points its README at the template here instead of the old WC-Generator source.

### Heads up

`auro sync` deletes the component's whole `.github/` folder before re-downloading it. Any local file in `.github/` that is not in this template is removed. It does not create a branch for you, so run it on a branch you are willing to change.

## More

- [auro-cli](https://github.com/AlaskaAirlines/auro-cli) for how `auro sync` works