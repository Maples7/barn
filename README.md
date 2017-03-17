# Barn
[![NPM](https://nodei.co/npm/barn-cli.png?downloads=true&downloadRank=true&stars=true)](https://nodei.co/npm/barn-cli/)
[![NPM](https://nodei.co/npm-dl/barn-cli.png?months=6&height=3)](https://nodei.co/npm/barn-cli/)       
A resume/CV generator, parsing information from YAML file and output a static website which you can deploy on the [Github Pages](https://pages.github.com/). Exactly like [Hexo](https://hexo.io/) for generating static resume website.

## Usage
### Installation
`npm install -g barn-cli`

### Workflow
0. `barn -h`: check the manual
1. `barn init`: init a barn folder using `git clone`, so make sure you are connecting to the `www`
2. `cd barn-starter`
3. fill `config.yml` with your own customized configs
4. fill YAML files in folder `content` with your own infomation
5. make use of `barn server` to debug your page and repeat step 3-5 until it satisfies you
6. `barn deploy`: deploy to your own github resume project
7. trun on Github Pages, see [https://pages.github.com/](https://pages.github.com/) for more instruction

### Commands API
- barn -h     
Checking the manual of this tool is the very first thing you should do.

- barn init / i    
Initiate a barn project using `git clone` with [Maples7/barn-starter](git@github.com:Maples7/barn-starter.git).

- barn genrate / g   
Generate ultimate static website to folder `dist`.

- barn server / s     
Watch any changes of any file and apply them to folder `dist` immediately, so you can browser `*.html` in folder `dist` to debug your page locally.

- barn deploy / d      
Deploy to a git-based server such as [Github Pages](https://pages.github.com/) and [Coding Pages](https://coding.net/help/doc/pages/).

- barn -v     
Check the version.

### Themes  
- default: the default theme of barn

You can download any themes above and put them in folder `themes` and apply any one of theme by change the config inside `Theme` block in `config.yml`.

(_Thers is only a default theme called `default` in folder `themes` for now, you are welcomed to customize your own and make it open source. If you'd like to, catch the key points of instruction below_)

#### How to make my own themes
Steps:
1. On Github, create a barn theme project
2. Put all html template in the root directory `./` and all css files in `./css`
3. Fully test and detail document are required in your own theme proejct
4. Post a PR to this project to list your own theme inside `Themes` above, please note whether any other template engines are needed besides `pug` and I'll give the support in my code
