# RunBook

Student Robotics Competition Program

[![CircleCI](https://circleci.com/gh/srobo/runbook.svg?style=svg)](https://circleci.com/gh/srobo/runbook)

# Installation

## Requirements

- Python (`>=3.5`)
- `pip`

## Usage

### Installing dependencies

```
pip install -r requirements.txt
```

### Running development server

```
mkdocs serve  # or ./scripts/serve
```

This will launch a server on http://localhost:8000. Content in the server will live-reload as changes are made. If large refactors of the site structure are made, it's advisable to stop the server, make the changes, then restart it.

### Production build

```
mkdocs build  # or ./scripts/build
```

This will build the site once, and place it in `site/` in the root of the project. This may be useful to see which files are rendered, and how exactly to access them.

### Tests

There are some rudimentary tests in the project. These are all run by the CI, and must pass before deployment.

```
./scripts/lint-yaml  # Checks the yaml content is well formatted
```

## Dependency management

Add any new dependencies to `requirements.in`, then run `pip-compile`.

To update existing dependencies, use `pip-compile --upgrade` for all or
`pip-compile --upgrade-package <name>` for a specific one.

If upgrading a dependency because this project's requirements have actually
changed (i.e: we now depend on a feature in a particular version), then instead
update the entry in `requirements.in` and run `pip-compile` as for a new
dependency.

## License

This work is licensed under the Creative Commons Attribution-ShareAlike 4.0
International License. To view a copy of this license, visit
http://creativecommons.org/licenses/by-sa/4.0/ or send a letter to Creative
Commons, PO Box 1866, Mountain View, CA 94042, USA.
