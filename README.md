[![Live Demo](https://img.shields.io/badge/Live%20Demo-quakeliveconfigeditor.com-red?style=for-the-badge&logo=quake)](https://quakeliveconfigeditor.com/)

# Quake Live Config Editor

> A visual web-based editor for Quake Live configuration files, optimized for **2026 competitive play**.  
> Generate professional `autoexec.cfg` files with a clean GUI — no more manual editing.

## Screenshots

![Quake Live Config Editor Action Binds](/assets/img/action-binds.jpg)

<p align="center">
  <img src="/assets/img/settings-general.jpg" width="49%" alt="Settings General" />
  <img src="/assets/img/enemy-skin-colors.jpg" width="49%" alt="Enemy Skin Colors" />
</p>

## ✨ Live Demo & Features

**Try it now:** [https://quakeliveconfigeditor.com/](https://quakeliveconfigeditor.com/)

### Core Features
- **Hundreds of confirmed 2026 CVARs** — Valid QL CVARs and recommended settings used by pros in the current Steam version
- **Complete binding system** — Every native action + advanced keys hidden in the normal menu
- **Advanced weapon aliases** — Individual scripts per weapon with multiple secondary binds
- **Custom scripting engine** — Rocket jumps, volume controls, and a built-in library of custom scripts/aliases
- **Config Importer** — Drop any `.cfg` file and watch it sync instantly with visual origin tracking
- **Cloud Save Slots** — 5 named profiles per account (Supabase sync across devices)
- **Live Filtered Search** + **Dynamic Dependency UI** — Settings appear/disappear based on master toggles
- **Commented & Smart-Aligned Export** — Beautiful, vertically structured `autoexec.cfg` with inline comments
- **Mobile-optimized** — Full touch support and portrait layout for both Tablet and Mobile
- **Manual Commit Mode** — Direct text editing in the preview pane with conflict detection

![Quake Live Config Editor Edit Custom Scripts](/assets/img/edit-custom-scripts.jpg)


## Cloud Config Modal
- **Save Up to 5 Configs** - Make custom names for your defined bind/scripts/settings.
- **Sync to CFG Editor** - Sync changes with a single click of a button.
- **Delete Option** - Delete a saved slot if room is needed to fit another.
- **Full User Control** - Add an email password for your Google or Discord auth, unsync auth methods.

![Quake Live Config Editor Cloud Controls Panel](/assets/img/cloud-controls-panel.jpg)

## 🛠️ Technical Stack

- **Frontend:** HTML5 + Tailwind CSS (CDN) + Vanilla JavaScript (zero heavy frameworks)
- **Backend/Auth:** Supabase (PostgreSQL, Auth, Cloud Storage)
- **Build Tools:** Terser, Clean-CSS, Prettier
- **Data:** Master `cvars.json` drives the entire UI
- **Deployment:** IONOS + Hostinger + Netlify (dev)

## 📁 Project Structure (Internal Reference)

```text
quakeliveconfigeditor.com/
├── index.html                 # Main editor layout + modals
├── assets/
│   ├── js/app.js              # Core logic, state management & Supabase
│   ├── js/comments.js         # Comments exported to .cfg for desktop editing
│   ├── data/cvars.json        # ~300 CVARs + UI metadata + pro tips
│   └── css/styles.css         # Tailwind overrides + caret (^color) rendering
├── cvars/                     # Auto-generated SEO database (300+ static pages)
├── generate-database.js       # Node.js script that builds the entire /cvars/ folder
├── build.sh                   # Production minification & deployment
├── build-test.sh              # Testing deployment script
├── _headers                   # Netlify/IONOS cache headers
├── 404.html
├── privacy.html
├── tos.html
├── robots.txt
├── sitemap.xml
└── llms.txt                   # Full AI context file (this README was built from it)
```

> **Note:** Full source code is private. This repository exists purely as a showcase for SEO, backlinks, and community reference.

## 🎯 Development Principles

- **Minimalism** — Vanilla JS only. Fast, maintainable, zero bloat.
- **Quake Authenticity** — Exact `seta`, `bind`, and `vstr` syntax. "Last-key-wins" import logic respected.
- **State-Driven UI** — Global state → `refresh()` cycle keeps everything in sync.
- **Schema-Based** — Everything generated from `cvars.json` (easy to add new settings).
- **SEO-First** — Static `/cvars/` pages auto-generated for every command.
- **Community Focused** — Built for 2026 tournament play with pro tips and recommended values baked in.

## 📊 Command Database

Every supported CVAR has its own dedicated page with:
- Description
- Default value
- Performance impact
- Pro tips
- Related commands
- Quick-copy `seta` command

**Browse the full database:** [https://quakeliveconfigeditor.com/cvars/](https://quakeliveconfigeditor.com/cvars/)

## 🤝 Support the Project

If this tool has helped you dominate in Quake Live, consider a small donation:

**[💛 Donate via PayPal](https://www.paypal.com/donate/?hosted_button_id=XQFKSUN94DZWA)**

Every contribution goes directly toward hosting and continued development.

## 📜 License

This project is **proprietary** (closed-source).  
The README, documentation, and generated CVAR database pages are released under **CC BY-NC-SA 4.0** for community reference.

## 👤 Author

**Ryan Bassett**  
Solo developer & longtime Quake Live player

🌐 **[Website](https://bassettgraphics.com)**  
𝕏 **[X / Twitter](https://x.com/razzabass)**  
💼 **[LinkedIn](https://www.linkedin.com/in/bassettr/)**  
🎮 **[Steam](https://steamcommunity.com/id/Holicc2/)**

---

**⭐ Star this repo** if you're using the editor — it helps with visibility and motivates future updates!

*Last updated: March 2026*
