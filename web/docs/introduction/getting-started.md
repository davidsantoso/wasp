---
title: Quick Start
slug: /quick-start
next: /tutorials/todo-app
---

import Tabs from '@theme/Tabs'
import TabItem from '@theme/TabItem'
import useBaseUrl from '@docusaurus/useBaseUrl';

## Installation

Welcome, new Waspeteer 🐝!

To install Wasp on Linux / OSX / WSL(Win), open your terminal and run: 

```shell
curl -sSL https://get.wasp-lang.dev/installer.sh | sh
```

 ℹ️ Wasp requires `node` and will warn you if it is missing: check below for [more details](#requirements).

Then, create a new app by running:

```shell
wasp new # Enter the project and choose the template
cd <my-project-name>
wasp start # Serves the web app.
```

That's it :tada:! You have successfully created and served a new web app at <http://localhost:3000> and Wasp is serving both frontend and backend for you.

:::info
Anything went wrong, or you have additional questions? Check [More Details](#more-details) section below!
:::


### What next?

 - [ ] 👉 **Check out the [Todo App tutorial](tutorials/todo-app.md) , which will take you through all the core features of Wasp!** 👈
 - [ ] If you are using VSCode, install our [Wasp language extension](https://marketplace.visualstudio.com/items?itemName=wasp-lang.wasp).
 - [ ] Join us on [Discord](https://discord.gg/rzdnErX)! Any feedback or questions you have, we are there for you.
 - [ ] Follow Wasp development by subscribing to our newsletter: https://wasp-lang.dev/#signup . We usually send 1 per month, and Matija does his best to unleash his creativity to make them engaging and fun to read :D!

------

## More details 

### Requirements

You must have `node` (and `npm`) installed on your machine and available in `PATH`. We rely on the latest Node.js LTS version (currently `v18.14.2`).

We recommend using [nvm](https://github.com/nvm-sh/nvm) for managing your Node.js installation version(s).

<details>
  <summary style={{cursor: 'pointer', 'textDecoration': 'underline'}}>
    Quick guide on installing/using nvm
  </summary>
  <div>

  Install nvm via your OS package manager (aptitude, pacman, homebrew, ...) or alternatively via [nvm install script](https://github.com/nvm-sh/nvm#install--update-script).

  Then, install a version of node that you need, e.g.:
  ```shell
  nvm install 18
  ```

  Finally, whenever you need to ensure a specific version of node is used, run e.g.
  ```shell
  nvm use 18
  ```
  to set the node version for the current shell session.

  You can run
  ```shell
  node -v
  ```
  to check the version of node currently being used in this shell session.

  Check NVM repo for more details: https://github.com/nvm-sh/nvm .

  </div>
</details>


### Installation

<Tabs
  defaultValue='linux/osx'
  values={[
    {label: 'Linux / OS X', value: 'linux/osx'},
    {label: 'Windows', value: 'win'},
    {label: 'From source', value: 'source'}
  ]}
>
  <TabItem value='linux/osx' >
<div style={{borderLeft: 'solid 6px #bf9900', paddingLeft: '10px'}} >

Open your terminal and run:

```shell
curl -sSL https://get.wasp-lang.dev/installer.sh | sh
```

</div>
  </TabItem>

  <TabItem value='win'>
<div style={{borderLeft: 'solid 6px #bf9900', paddingLeft: '10px'}} >

With Wasp for Windows, we are almost there: Wasp is successfully compiling and running on Windows but there is a bug or two stopping it from fully working. Check it out [here](https://github.com/wasp-lang/wasp/issues/48) if you are interested in helping.

In the meantime, the best way to start using Wasp on Windows is by using [WSL](https://docs.microsoft.com/en-us/windows/wsl/install-win10). Once you set up Ubuntu on WSL, just follow Linux instructions for installing Wasp. If you need further help, reach out to us on [Discord](https://discord.gg/rzdnErX) - we have some community members using WSL that might be able to help you.

:::caution
  If you are using WSL2, make sure that your Wasp project is not on Windows file system, but instead on Linux file system. Otherwise, Wasp won't be able to detect file changes, due to the [issue in WSL2](https://github.com/microsoft/WSL/issues/4739).
:::

</div>
  </TabItem>

  <TabItem value='source'>
<div style={{borderLeft: 'solid 6px #bf9900', paddingLeft: '10px'}} >

If the installer is not working for you or your OS is not supported, you can try building Wasp from source.

To install from source, you need to clone the [wasp repo](https://github.com/wasp-lang/wasp), install [cabal](https://cabal.readthedocs.io/en/stable/getting-started.html) on your machine and then run `cabal install` from the `waspc/` dir.

If you have never built Wasp before, this might take some time due to `cabal` downloading dependencies for the first time.

Check [waspc/](https://github.com/wasp-lang/wasp/tree/main/waspc) for more details on building.

</div>
  </TabItem>
</Tabs>


:::tip Try Wasp Without Installing 🤔?
  Give Wasp a spin in the browser without any setup by running our [Wasp Template for Gitpod](https://github.com/wasp-lang/gitpod-template)
:::
