## [My GitHub](https://github.com/elenalomova) | My website: [www.elenalomova.online](https://elenalomova.online/) | My [Substack](https://blog.elenalomova.online/) | My [LinkedIn](https://www.linkedin.com/in/elena-lomova/)

## August 12, 2026

An update on my two Obsidian plugins — over the past year they've grown quite a bit and even changed their names.

The plugin that groups notes by tags used to be called `maps-of-content`, now it's **Content by Tags** (`content-by-tags`): [github.com/elenalomova/Obsidian-content-by-tags](https://github.com/elenalomova/Obsidian-content-by-tags). What's new:

- the tag map is now laid out as a table with three columns — the date of the most recent note under that tag, the note count, and a collapsible list (`<details>`, collapsed by default);
- the sort order can be changed from settings or via three command-palette commands (by name / by note count / by most recent note date) — a ↓ arrow in the table header shows which column is currently active;
- notes without tags and the `Obsidian` tag are always pinned as the first two rows, everything else follows the chosen sort order;
- support for nested tags (`project/work/client`) and the ability to exclude specific tags from the map;
- a language switch (Russian / English) was added to the settings — it also changes the text of the generated map itself.

If you're upgrading from the old version: the plugin id changed from `maps-of-content` to `content-by-tags`, so Obsidian will treat it as a new plugin — you'll need to enable it again, and the old `maps-of-content` folder under `.obsidian/plugins/` can be removed.

The second plugin, which used to build a map based on folder structure, was previously called "Vault Map Generator" (`vault-map-generator`), now it's **Content by Folders** (`content-by-folders`): [github.com/elenalomova/Obsidian-content-by-folders](https://github.com/elenalomova/Obsidian-content-by-folders). It got a solid upgrade too:

- subfolders are now shown as toggles nested inside one another — the toggle structure mirrors your actual folder hierarchy;
- two new settings, "Second-level folders as separate rows" and "Third-level folders as separate rows", let you pull subfolders one or two levels deep out into their own table row instead of hiding them inside the parent's list;
- files sitting directly in the vault root always come first, labeled "No folder";
- the same table-sorting logic (by name / by file count / by modification date) via settings or commands, with the same ↓ arrow in the header;
- you can now exclude notes by tag (not just by folder), and filter by file type — toggling images and PDFs on or off.

The id changed here too: from `vault-map-generator` to `content-by-folders`, so on upgrade you'll need to enable the plugin again, and the old `vault-map-generator` folder can be removed.

Both plugins are still installed manually: download `main.js` and `manifest.json` from GitHub, put them into `.obsidian/plugins/content-by-tags/` and `.obsidian/plugins/content-by-folders/` respectively, restart Obsidian, and enable them in Settings → Community Plugins.

Download and follow: [github.com/elenalomova](https://github.com/elenalomova)


## August 9, 2026

New project: a **Pulya Calculator** for Preferans, built under the "Leningrad" convention: [github.com/elenalomova/pref](https://github.com/elenalomova/pref)

It's a self-contained HTML/CSS/JS widget that calculates the final settlement (the "pulya") for a game of Preferans — no build step, no external JS libraries, just the two Google Fonts it uses. You drop the whole file's contents straight into a page. Both language versions are ready to be pasted directly into a T123 block on Tilda, and you can see them live here:

- 🇷🇺 Russian version: [elenalomova.online/projects/pref](https://elenalomova.online/projects/pref)
- 🇬🇧 English version: [elenalomova.online/projects/pref/en](https://elenalomova.online/projects/pref/en)

What it does:

- switches between **3- and 4-player modes** with one click;
- has two layouts — a card grid for narrow screens, and a compass-style diagram (from 640px wide) that mirrors the score sheet from the source book, with the gora in the center, pulya in the middle ring, and whists on the outer edge;
- validates input as you type — name fields only take letters and digits (max 10 characters), numeric fields only take whole numbers from 0 to 9999;
- runs the settlement automatically, following the three-step Leningrad convention algorithm: the pulya adjusts each player's gora relative to the group average, the adjusted gora gets converted into whists, and then whists from play and whists from the gora are combined into the final result;
- flags a warning if the final results across all players don't sum to zero, which usually means there's a typo somewhere;
- has an expandable per-player breakdown — average pulya, adjusted gora, gora debt, and net result against each opponent.

The algorithm itself follows Nikolai Rozaliev's book *"Preferans. Bridge"*.

Download and follow: [github.com/elenalomova](https://github.com/elenalomova)


## August 22, 2025

I vibe-coded two plugins for my Obsidian using Claude: one generates a note where all existing notes are grouped by tags, the other generates a note where all notes are grouped by folder structure (similar to a sitemap.xml). You take the files from [github](https://github.com/elenalomova) and put them in `Obsidian \ .obsidian \ plugins`, launch Obsidian, enable the plugins in settings, restart Obsidian, and voilà — everything generates and updates automatically ✨

All of this is needed for the [Gemini Scribe](https://www.obsidianstats.com/plugins/gemini-scribe) plugin, connected for free via [Google AI Studio](https://ai.google.dev/gemini-api/docs/pricing) (click "Try it in Google AI Studio"): the Gemini Scribe chat works within the context of the currently open note — it reads it, follows the links in it to your other notes, and answers your questions in chat (the depth of traversal is set in the Context Depth field). So the note lists generated through my two plugins help you build a note for processing through Gemini Scribe simply via ctrl+c, ctrl+v.

Next level shit! Download the plugins and follow: [github.com/elenalomova](https://github.com/elenalomova)
