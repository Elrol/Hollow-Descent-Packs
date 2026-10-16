# Hollow Descent Packs Repository

Welcome to the official pack registry and repository for **Hollow Descent**, a data-driven action roguelike developed by Arrowsend Studio LLC. 

This repository hosts the central pack registry (`pack_registry.json`), approved community mod packs, custom tiles, rooms, and levels designed to expand the game.

---

## Repository Structure

* `pack_registry.json` — The master registry listing all approved community and official packs, including their manifest URLs, repository links, and download links.
* `packs/` — Contains individual pack folders (such as the `example` pack), each containing their own `manifest.json` and modular asset directories (`rooms/`, `levels/`, `tiles/`).

---

## Automated CI/CD Validation

To ensure all community submissions integrate cleanly without breaking the game, this repository utilizes a GitHub Actions workflow (`validate_packs.yml`). 

Every push or pull request automatically triggers:
1. **JSON Syntax Checks:** Validates that all registry and manifest files are correctly formatted.
2. **Schema & Key Verification:** Ensures required keys (such as `id`, `name`, `author`, `version`, and `min_game_version`) are present.
3. **Live HTTP Status Checks:** Verifies that all registered download URLs and manifest links return a valid `200 OK` status code.

---

## How to Submit Your Own Pack

Want to add your custom pack (like a spooky Halloween expansion) to the in-game Pack Manager? Follow these steps:

1. **Build Your Pack:** Create a folder in your local environment with a unique namespace containing your `manifest.json`, rooms, levels, and tiles.
2. **Host Your Files:** Create a public GitHub repository for your pack, create a GitHub Release containing a `.zip` archive of your pack files, and ensure your `manifest.json` is accessible via a raw link.
3. **Submit an Entry:** Add your pack details to the `pack_registry.json` file in this repository under the approved packs list.
4. **Pass CI Validation:** Submit a pull request. Once the GitHub Actions workflow successfully validates your schema and links, your pack will be reviewed and merged into the registry, making it instantly downloadable for players in-game!

---

## License

Please refer to individual pack directories for specific licensing terms. Core game and template files follow Arrowsend Studio LLC distribution guidelines.