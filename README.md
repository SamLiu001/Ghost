&nbsp;

## 使用我们自己修改过的 ghost 包来安装或更新
## 为防止 ghost update 命令更新了官方的包，确保我们的包版本号始终比官方高
## 我们自己包的发行版本：https://api.github.com/repos/SamLiu001/Ghost/releases

### install.sh
```shell
export update_zip_url=https://api.github.com/repos/SamLiu001/Ghost/zipball/v4.43.5;

rm -rf ./._temp_ghost.zip && rm -rf ./myghost.zip && rm -rf ./.myghost && curl -L -o ._temp_ghost.zip $update_zip_url && unzip ._temp_ghost.zip -d .myghost && cd .myghost && cd $(ls -d */|head -n 1) && zip -r ../../myghost.zip . && cd ../../ && rm -rf ./._temp_ghost.zip && rm -rf ./.myghost && ghost install --zip myghost.zip && rm -rf ./myghost.zip
```

### update.sh
```shell
export update_zip_url=https://api.github.com/repos/SamLiu001/Ghost/zipball/v14.42.1;

rm -rf ./._temp_ghost.zip && rm -rf ./myghost.zip && rm -rf ./.myghost && curl -L -o ._temp_ghost.zip $update_zip_url && unzip ._temp_ghost.zip -d .myghost && cd .myghost && cd $(ls -d */|head -n 1) && zip -r ../../myghost.zip . && cd ../../ && rm -rf ./._temp_ghost.zip && rm -rf ./.myghost && ghost update --zip myghost.zip && rm -rf ./myghost.zip
```

<p align="center">
  <a href="https://ghost.org/#gh-light-mode-only" target="_blank">
    <img src="https://user-images.githubusercontent.com/65487235/157884383-1b75feb1-45d8-4430-b636-3f7e06577347.png" alt="Ghost" width="200px">
  </a>
  <a href="https://ghost.org/#gh-dark-mode-only" target="_blank">
    <img src="https://user-images.githubusercontent.com/65487235/157849205-aa24152c-4610-4d7d-b752-3a8c4f9319e6.png" alt="Ghost" width="200px">
  </a>
</p>
&nbsp;

<p align="center">
    <a href="https://ghost.org/">Ghost.org</a> •
    <a href="https://forum.ghost.org">Forum</a> •
    <a href="https://ghost.org/docs/">Docs</a> •
    <a href="https://github.com/TryGhost/Ghost/blob/master/.github/CONTRIBUTING.md">Contributing</a> •
    <a href="https://twitter.com/ghost">Twitter</a>
    <br /><br />
    <a href="https://ghost.org/">
        <img src="https://img.shields.io/badge/downloads-2M-brightgreen.svg" alt="Downloads" />
    </a>
    <a href="https://github.com/TryGhost/Ghost/releases/">
        <img src="https://img.shields.io/github/release/TryGhost/Ghost.svg" alt="Latest release" />
    </a>
    <a href="https://github.com/TryGhost/Ghost/actions">
        <img src="https://github.com/TryGhost/Ghost/workflows/Test%20Suite/badge.svg?branch=main" alt="Build status" />
    </a>
    <a href="https://github.com/TryGhost/Ghost/contributors/">
        <img src="https://img.shields.io/github/contributors/TryGhost/Ghost.svg" alt="Contributors" />
    </a>
</p>
<p align="center">
  Love open source? <a href="https://careers.ghost.org/product-engineer-node-js/">We're hiring</a> Node.js engineers to work on Ghost full-time.
</p>

&nbsp;

<a href="https://ghost.org/"><img src="https://user-images.githubusercontent.com/120485/66918181-f88fdc80-f048-11e9-8135-d9c0e7b35ebc.png" alt="Fiercely independent, professional publishing. Ghost is the most popular open source, headless Node.js CMS which already works with all the tools you know and love." /></a>
&nbsp;

<a href="https://ghost.org/pricing/#gh-light-mode-only" target="_blank"><img src="https://user-images.githubusercontent.com/65487235/157849437-9b8fcc48-1920-4b26-a1e8-5806db0e6bb9.png" alt="Ghost(Pro)" width="165px" /></a>
<a href="https://ghost.org/pricing/#gh-dark-mode-only" target="_blank"><img src="https://user-images.githubusercontent.com/65487235/157849438-79889b04-b7b6-4ba7-8de6-4c1e4b4e16a5.png" alt="Ghost(Pro)" width="165px" /></a>

The easiest way to get a production instance deployed is with our official **[Ghost(Pro)](https://ghost.org/pricing/)** managed service. It takes about 2 minutes to launch a new site with worldwide CDN, backups, security and maintenance all done for you.

For most people this ends up being the best value option cause of [how much time it saves](https://ghost.org/docs/hosting/) — and 100% of revenue goes to the Ghost Foundation; funding the maintenance and further development of the project itself. So you’ll be supporting open source software *and* getting a great service!

If you prefer to run on your own infrastructure, we also offer official 1-off installs and managed support and maintenance plans via **[Ghost(Valet)](https://valet.ghost.org)** - which can save a substantial amount of developer time and resources.

&nbsp;

# Quickstart install

If you want to run your own instance of Ghost, in most cases the best way is to use our **CLI tool**

```
npm install ghost-cli -g
```

&nbsp;

Then, if installing locally add the `local` flag to get up and running in under a minute - [Local install docs](https://ghost.org/docs/install/local/)

```
ghost install local
```

&nbsp;

or on a server run the full install, including automatic SSL setup using LetsEncrypt - [Production install docs](https://ghost.org/docs/install/ubuntu/)

```
ghost install
```

&nbsp;

Check out our [official documentation](https://ghost.org/docs/) for more information about our [recommended hosting stack](https://ghost.org/docs/hosting/) & properly [upgrading Ghost](https://ghost.org/docs/update/), plus everything you need to develop your own Ghost [themes](https://ghost.org/docs/themes/) or work with [our API](https://ghost.org/docs/content-api/).

### Contributors & advanced developers

For anyone wishing to contribute to Ghost or to hack/customize core files we recommend following our full development setup guides: [Contributor guide](https://ghost.org/docs/contributing/) • [Developer setup](https://ghost.org/docs/install/source/) • [Admin Client dev guide](https://ghost.org/docs/install/source/#ghost-admin)

&nbsp;

# Ghost sponsors

We'd like to extend big thanks to our sponsors and partners who make Ghost possible. If you're interested in sponsoring Ghost and supporting the project, please check out our profile on [GitHub sponsors](https://github.com/sponsors/TryGhost) :heart:

**[DigitalOcean](https://m.do.co/c/9ff29836d717)** • **[Fastly](https://www.fastly.com/)**

&nbsp;

# Getting help

You can find answers to a huge variety of questions, along with a large community of helpful developers over on the [Ghost forum](https://forum.ghost.org/) - replies are generally very quick. **Ghost(Pro)** customers also have access to 24/7 email support.

To stay up to date with all the latest news and product updates, make sure you [subscribe to our blog](https://ghost.org/blog/) — or you can always follow us [on Twitter](https://twitter.com/Ghost), if you prefer your updates bite-sized and facetious. :saxophone::turtle:

&nbsp;

# Copyright & license

Copyright (c) 2013-2022 Ghost Foundation - Released under the [MIT license](LICENSE). Ghost and the Ghost Logo are trademarks of Ghost Foundation Ltd. Please see our [trademark policy](https://ghost.org/trademark/) for info on acceptable usage.
