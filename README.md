# steamdeckdocs
Community driven markdown documentation for the steamdeck that will generate static html on https://steamdeckdocs.org.

## Used software

**Linting with markdownlint**: [markdownlint](https://github.com/markdownlint/markdownlint)
**Creating static html with mkdocs**: [mkdocs](https://www.mkdocs.org/)

### How to install

#### Debian 12
```
apt install ruby-mdl mkdocs
```

### How to use

**Checking if the new files are valid**: `mdl docs/`
**Building a new page**: `mkdocs build` (See site/ for the static html)

## TODO
- Pipelines for deploying website
- Where to store images?
- Add steamdeck icons that you can easily use in the markdown
- Create a styleguide so we will have somewhat unified docs
- Add [header enumerating plugin](https://github.com/timvink/mkdocs-enumerate-headings-plugin)
- Create more documentation
- Maybe create a more steamdeck styled theme?
