# Student Robotics Volunteer Runbook

[![GitHub Actions](https://github.com/srobo/runbook/actions/workflows/main.yml/badge.svg?branch=main)](https://github.com/srobo/runbook/actions/workflows/main.yml)

The runbook aims to be a single source for all Student Robotics internal
documentation. This includes information for the [Competition Team][competition-team]
and [Kit Team][kit-team], as well as other activities.

[competition-team]: https://opsmanual.studentrobotics.org/annual-robotics-competition/competition-team
[kit-team]: https://opsmanual.studentrobotics.org/annual-robotics-competition/kit-team

## Installation

To run this project locally, you'll need:

- Python (`>=3.6, <3.12`)
- `pip`

## Usage

### Installing dependencies

It's recommended to use a [virtual environment](https://docs.python.org/3/tutorial/venv.html):

```
python -m venv env

env\Scripts\activate.bat  # on windows
source env/bin/activate  # on macOS / Linux
```

Then, install dependencies:

```
pip install -r requirements.txt
```

### Running development server

```
mkdocs serve
```

This will launch a server on http://localhost:8000. Content in the server will live-reload as changes are made. If large refactors of the site structure are made, it's advisable to stop the server, make the changes, then restart it.

### Production build

```
mkdocs build
```

This will build the site once, and place it in `site/` in the root of the project. This may be useful to see which files are rendered, and how exactly to access them.

### Spell checking

This project uses [CSpell](https://cspell.org/) for spell checking. Plugins are
available for a variety of editors and a command line runner is available
through `npm`:

```
npm install
```

```
npm run spell-check
```

Words that CSpell is unaware of can be added to the `.spelling` file.

## License

This work is licensed under the Creative Commons Attribution-ShareAlike 4.0
International License. To view a copy of this license, visit
http://creativecommons.org/licenses/by-sa/4.0/ or send a letter to Creative
Commons, PO Box 1866, Mountain View, CA 94042, USA.
