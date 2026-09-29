# Pokémon Finder & Comparison Tool

A browser-based app for looking up Pokémon, comparing their stats and type matchups, and building balanced teams. It uses data from the [PokéAPI](https://pokeapi.co/).

## Features

- Search by Pokémon name or Pokédex number and explore stats, abilities, moves, and type effectiveness.
- Compare two Pokémon side by side, including stats and shared or unique type matchups.
- Build a team of up to six Pokémon, review team coverage, and get recommendations.
- Filter searches and recommendations by generation; filter recommendations by type and sort them.
- Save and reload a team in your browser.
- Switch between English and Spanish and light and dark themes.
- Installable app shell with a service worker; previously cached app files can load offline.

## Get started

### Requirements

- A modern browser and an internet connection for Pokémon data and the Tailwind CSS CDN.
- Python 3 or another local HTTP server. There is no package manifest or build step.

### Run locally

Clone the repository, start a local server from its directory, and open the local address in your browser:

```bash
git clone https://github.com/VoidLance/course-files-javascript-pokemonapi.git
cd course-files-javascript-pokemonapi
python3 -m http.server 8000
```

Visit <http://localhost:8000>. Serving over HTTP on `localhost` also allows the service worker to register; opening `index.html` directly does not.

### Use the app

1. Enter a Pokémon name or number (for example, `pikachu` or `25`) and select **Search**.
2. Enter another Pokémon and select **Compare** to see both results and the comparison summary.
3. Choose **Build Team** to add Pokémon to team slots, review recommendations, and save or reload your team.
4. Use the generation, language, and theme controls to customize the results and interface.

The service worker caches the app shell, not PokéAPI data. Pokémon lookups require an internet connection.

## Project files

- `index.html` — application interface; loads Tailwind CSS from its CDN.
- `script.js` — search, comparison, team-building, and API logic.
- `styles.css` — application styles.
- `sw.js` and `manifest.webmanifest` — offline app shell and install metadata.
- [QUICK-REFERENCE.md](QUICK-REFERENCE.md) — code and feature reference.

## Help

- For app questions or bug reports, [open an issue](https://github.com/VoidLance/course-files-javascript-pokemonapi/issues).
- For Pokémon data/API information, see the [PokéAPI documentation](https://pokeapi.co/docs/v2).
- For web platform questions, see [MDN Web Docs](https://developer.mozilla.org/).

## Contributing and maintenance

The project is maintained in [VoidLance/course-files-javascript-pokemonapi](https://github.com/VoidLance/course-files-javascript-pokemonapi). Contributions are welcome: open an issue to discuss a change, then submit a pull request with a clear description and verify the app in a browser. This repository does not currently include a separate contribution guide or automated test/build commands.

Pokémon data is provided by [PokéAPI](https://pokeapi.co/). The repository does not currently include a `LICENSE` file; check with the maintainers before redistributing the project.
