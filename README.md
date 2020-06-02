# Preons 🛰

A functional CSS system for building user interfaces 🛰

[Documentation](#-documentation) | [CLI](#-cli) | [Reference](#-reference) | [Roadmap](#-roadmap)

![](docs/notes/images/preons-tech.png)

## 🔬Currently Under Development

This repo is subject to lots of changes as it's in prime experimental mode. See _going from [0.0.0 to 1.0.0](/docs/notes/2020-05.md#experimental-mode)_.

## 🚀 Documentation

Get started [here](https://www.preons.co/learn/#build-the-ui).

## 💠 Themes

Coming soon

## 💻 CLI

<!-- Config -->

```bash
Usage: preons [options] [command]

Options:
  -V, --version      output the version number
  -h, --help         display help for command

Commands:
  stylesheet [name]  Generates a stylesheet
  config [name]      Converts config
  help [command]     display help for command
```

<!-- Config -->

## 🗒 Configuration

Example [preons.yaml](/config/preons.yaml).

### Preons yaml structure

```yaml
preons:
  baseline: # Baseline rule

  rules:
    # Object reusable rules

  properties:
    # Css properties

  breakpoints:
    # Stylesheet breakpoints
```

### Baseline

This is the vertical rhythm of your stylesheet.

### Rules

These are reusable rules across multiple css properties.

```yaml
preons:
  theme-colors:
    black: "#242027"
    white: "#f4f2f9"
    greyl: "#beb9cc"
    grey: "#7d778e"
    greyd: "#312948"
    transparent: "transparent"
    hotpink: "#ea2889"
```

### Properties

These are css properties and the functional css prefix.

## Preonize Function

The `preonize` function is currently an `scss` function. It allows Preons to generate lots of rules at multiple breakpoints without having to hardcode each CSS class.

It has 4 parameters.

```plain
@include preonize(
  <class name>,       # The prefix name of the class eg. 'h' for height
  <css property>,     # The css property assigned to the class 'height'
  <sass map rules>,   # Sass map of rules eg. (1: 1rem, 2: 2rem)
  <breakpoints>       # Breakpoints
);
```

Thus, we can reuse different sass-maps for several rules. Here's an example use:

```scss
@include preonize(
  "h",
  width,
  map-collection(scaled, percentaged, discrete, special-sizes),
  $breakpoints
);
```

## 📚 Reference

Look up the reference [here](https://preons.netlify.app/search) or peruse them below.

## 🛠 Functional CSS

Coming soon

## 🗺️ Roadmap

My mission with Preons is to componentize the Web's UI and make building them fast, systemized, and available to all sorts of people regardless of coding ability.

- [ ] Preons documentation
- [x] Cheatsheet lookup (reference)
- [x] Configuaration syntax
- [ ] CLI
  - [x] Sass generator
  - [x] Css generator
  - [x] References generator
  - [x] Documentation generator
  - [ ] Components generator
  - [ ] Reverse generator. Create preons.yaml from functional css styles
- [ ] Tests
  - [ ] CLI
  - [ ] UI

## ⛓ Versioning

This project uses [SemVer](http://semver.org/) for versioning and [Intuit's Auto](https://intuit.github.io/auto/) to generate releases on the fly. For the versions available, see the [tags on this repository](https://github.com/preons/preons/tags).

## 🙌 Thank yous

- [Intuit's Auto](https://intuit.github.io/auto/) for making releases easier
- [Unsplash](https://unsplash.com/) for the title image
- [Adam Moore & Tachyons](https://tachyons.io/) for creating their wonderful library

## 🔖 Licence

You are free to modify and do as you choose to this library however, it uses [GPLv2.1](#LICENSE) to keep it free for all into the future. Of course, you can commercialize your product where this library is part of a larger piece of work and is merely a dependency.

Here's a really helpful video explanation of GPL licences in general.

https://www.youtube.com/watch?v=JlIrSMzF8T4

## Contributors ✨

Thanks goes to these wonderful people ([emoji key](https://allcontributors.org/docs/en/emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<table>
  <tr>
    <td align="center"><a href="http://getrentr.com"><img src="https://avatars0.githubusercontent.com/u/4562670?v=4" width="100px;" alt=""/><br /><sub><b>Gemma Black</b></sub></a><br /><a href="https://github.com/preons/preons/commits?author=gemmadlou" title="Documentation">📖</a> <a href="https://github.com/preons/preons/commits?author=gemmadlou" title="Code">💻</a> <a href="https://github.com/preons/preons/commits?author=gemmadlou" title="Tests">⚠️</a></td>
    <td align="center"><a href="https://github.com/pgrimaud"><img src="https://avatars1.githubusercontent.com/u/1866496?v=4" width="100px;" alt=""/><br /><sub><b>Pierre Grimaud</b></sub></a><br /><a href="https://github.com/preons/preons/commits?author=pgrimaud" title="Documentation">📖</a></td>
  </tr>
</table>

<!-- markdownlint-enable -->
<!-- prettier-ignore-end -->
<!-- ALL-CONTRIBUTORS-LIST:END -->

This project follows the [all-contributors](https://github.com/all-contributors/all-contributors) specification. Contributions of any kind welcome!
