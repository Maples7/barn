# Barn

[![NPM](https://nodei.co/npm/barn-cli.png?downloads=true&downloadRank=true&stars=true)](https://nodei.co/npm/barn-cli/)
[![NPM](https://nodei.co/npm-dl/barn-cli.png?months=6&height=3)](https://nodei.co/npm/barn-cli/)  
**[Online Demo](http://cv.maples7.com/)**  
A resume/CV generator, parsing information from YAML file to generate a static website which you can deploy on the [Github Pages](https://pages.github.com/). Exactly like resume-version [Hexo](https://hexo.io/).

## Usage

### Installation

`[sudo] npm install -g barn-cli` or `[sudo] yarn global add barn-cli`  
(_Of course, you should install [Node.js with npm](https://nodejs.org/en/download/) before that_)

### Workflow

0. `barn -h`: check the manual
1. `barn init`: init a barn folder using `git clone`, so make sure you are connecting to the `www`
1. `cd barn-starter`
1. fill `config.yml` with your own customized configs
1. fill YAML files in folder `themes/${your theme}/content/` with your own information
1. make use of `barn server` to debug your pages and repeat step 3-5 until it satisfies you
1. `barn deploy`: deploy to your own github resume repository
1. trun on Github Pages, see [https://pages.github.com/](https://pages.github.com/) for more instruction

### Commands

- barn -h  
  Checking the manual of this tool is the very first thing you should do.

- barn init / i  
  Initiate a barn project using `git clone` with [Maples7/barn-starter](https://github.com/Maples7/barn-starter).

- barn genrate / g  
  Generate ultimate static website to folder `dist`.

- barn server / s  
  Watch any changes of any files and apply them to folder `dist` immediately, so you can open `*.html` in folder `dist` with your browser to debug your pages locally.

- barn deploy / d  
  Deploy to a git-based server such as [Github Pages](https://pages.github.com/) and [Coding Pages](https://coding.net/help/doc/pages/).

- barn -v  
  Check the version.

### Themes

- default: the default theme of barn

You can download any themes above and put them in folder `themes` and apply any one of them by changing the config inside `Theme` block in `config.yml`.

(_Thers is only a theme called `default` in folder `themes` for now, you are welcomed to customize your own and make it open source. If you'd like to, catch the key points of instruction below._)

#### How to make my own themes

Steps:

1. On Github, create a barn theme project whose name is supposed to follow pattern `barn-theme-XXXX`
2. Put all html templates in the root directory `./`, all css files in `./css/` and all images in `./image/`
3. Make starter YAML files for information needed to render pages in `./content/` to tell users what they should provide
4. Full tests and detail document are required in your own theme project
5. Post a PR to this project to list your own theme inside `Themes` block above, please note whether any other template engines are needed besides `pug` and I'll give some support in my code

You are welcomed to review this project for more information you need.

## Debug

`DEBUG=barn-cli barn [command]`: add `DEBUG=barn-cli` at the beginning of any command to get more information about the running status of program.

## Relatives

- [barn-starter](https://github.com/Maples7/barn-starter)
- [barn-cli](https://github.com/Maples7/barn-cli)

## Contributors

- [Maples7](http://maples7.com/): Creator and maintainner of this project
- [ShadowWood](https://shadowwood.me/): Maker of the `default` theme

## License

[MIT](LICENSE)
