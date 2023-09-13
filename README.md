# steamdeckdocs

Community driven markdown documentation for the steamdeck that generates static html through [mkdocs](https://www.mkdocs.org/) on https://steamdeckdocs.org.

## Local testing

#### Needed software

**Debian 12**

```
apt install ruby-mdl mkdocs
```

**Arch**
```
pacman -S markdownlint
yay -S mkdocs
```

### Testing markdown

```
mdl docs/
```

### Checking your changes

Run the below command and point your browser to http://localhost:8000

```
mkdocs serve
```

## TODO

Check out the [@tuxx's steamdeckdocs todo board](https://github.com/users/tuxx/projects/1/views/1)

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for more info
