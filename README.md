# Barn

[![NPM](https://nodei.co/npm/barn-cli.png?downloads=true&downloadRank=true&stars=true)](https://nodei.co/npm/barn-cli/)
[![NPM](https://nodei.co/npm-dl/barn-cli.png?months=6&height=3)](https://nodei.co/npm/barn-cli/)

**[Online Demo](http://cv.maples7.com/)**

A resume/CV static site generator — parse your information from YAML files plus Pug templates, and output a deployable static website. Think of it as a resume-focused [Hexo](https://hexo.io/). Deploy effortlessly to [GitHub Pages](https://pages.github.com/) or any static hosting service.

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/en/download/) (with npm)

### Installation

```bash
npm install -g barn-cli
# or
yarn global add barn-cli
```

### Workflow

1. **Initialize a project**

   ```bash
   barn init
   cd barn-starter
   ```

   This clones the [barn-starter](https://github.com/Maples7/barn-starter) template and removes the `.git` directory so you can start fresh.

2. **Configure**

   Edit `config.yml` to set your preferred theme, deploy repository, custom domain (CNAME), and other options.

3. **Fill in your information**

   Edit YAML files under `themes/<your-theme>/content/` with your personal details (profile, education, work experience, skills, etc.). Each YAML file corresponds to a page — for example, `index.yml` for the Chinese version and `en.yml` for the English version.

4. **Preview locally**

   ```bash
   barn server
   ```

   This starts an HTTP dev server (default port **3579**) with **live reload**. Any file changes are detected automatically — the pages regenerate and refresh in your browser in real time. Repeat steps 2–3 until you are satisfied.

5. **Deploy**

   ```bash
   barn deploy
   ```

   This generates the final static site into `dist/`, then pushes it to the remote repository configured in `config.yml`. Turn on GitHub Pages for your repo ([instructions](https://pages.github.com/)) and your resume will be live.

### Commands

| Command | Alias | Description |
|---|---|---|
| `barn init` | `barn i` | Clone the [barn-starter](https://github.com/Maples7/barn-starter) template to bootstrap a new project. |
| `barn generate` | `barn g` | Render Pug templates with YAML data, minify HTML/CSS, and output the static site to `dist/`. |
| `barn server` | `barn s` | Generate the site, start a dev server with live reload, and open it in the browser. Use `-p <port>` to specify a custom port. |
| `barn deploy` | `barn d` | Generate the site and deploy to a git-based hosting service (e.g., [GitHub Pages](https://pages.github.com/)). |
| `barn -v` | | Show the version. |
| `barn -h` | | Show the help manual. |

### Themes

| Theme | Description |
|---|---|
| `default` | Two-column layout with a gray sidebar. |
| `latex` | LaTeX-style academic resume — single-column, serif fonts, horizontal rules, print-friendly. |

To switch themes, change the `theme` field in `config.yml`. You can also place additional themes in the `themes/` directory.

Contributions of new themes are welcome! See below for guidelines.

#### Creating a Custom Theme

1. Create a repository named following the pattern `barn-theme-XXXX`.
2. Place Pug templates in the root directory (`./`), CSS files in `./css/`, and images in `./image/`.
3. Provide starter YAML files in `./content/` so users know what data fields to fill in.
4. Include a README with documentation and usage instructions.
5. Submit a PR to this project to have your theme listed above. If your theme requires a template engine other than Pug, please note that in the PR.

## Debug

Prefix any command with `DEBUG=barn-cli` to enable verbose logging:

```bash
DEBUG=barn-cli barn server
```

## Related

- [barn-cli](https://github.com/Maples7/barn-cli) — The CLI tool
- [barn-starter](https://github.com/Maples7/barn-starter) — The starter template

## Contributors

- [Maples7](http://maples7.com/) — Creator and maintainer
- [ShadowWood](https://shadowwood.me/) — Author of the `default` theme

## License

[MIT](LICENSE)
