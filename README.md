# Camunda theme for Hugo docs

## Install

Clone this repository/branch aside of the `docs.camunda.org`

```sh
# from the docs.camunda.org directory
cd ..
git clone git@github.com:camunda/docs.camunda.org.git docs-hugo-theme
# go into its directory
cd docs-hugo-theme
git checkout docs-hugo-styling
npm i
grunt build
```

_Note:_ you can clone this repository anywhere,
but you may then change the `setup.target` value of `package.json`.

## Working

After installing (you probably want to have [hugo running as watching server][building-docs])
and then use `grunt` in this directory.

## Consuming the theme

The simplest way to consume the theme in a project is to use the git subtree facilitites:

Adding the latest version of the theme as `camunda`:

```bash
git subtree add -P themes/camunda git@github.com:camunda/camunda-docs-theme.git dist --squash
```

Updating the theme to the latest version:

```bash
git subtree pull -P themes/camunda git@github.com:camunda/camunda-docs-theme.git dist --squash
```

### Theme development with Virtualbox

This would be the command to execute in order to make the local development site
of `camunda-docs-manual` (see `--baseUrl` option) available in a virtualbox (typically for IE).
Livereload should be deactivate (see `--disableLiveReload`) if you want to develop for IE9.

```sh
hugo --bind="0.0.0.0" --baseUrl="http://10.0.2.2:1313/manual/develop/" -w --disableLiveReload=true server
```
The development site is then available on `http://10.0.2.2:1313/manual/develop/``in your virtualbox
guest OS.

## Licence

[MIT](LICENSE)


[building-docs]: https://github.com/camunda/docs.camunda.org/tree/hugo#building-the-doumentation
