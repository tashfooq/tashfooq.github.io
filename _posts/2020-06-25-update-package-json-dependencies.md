---
title: Keeping package.json dependencies up to date
date: 2020-06-25
categories:
- node
- npm
---
### Why this is important
I'm currently working on a project with a React front-end and PHP back-end. Which is why I couldn't just something like

<!-- more -->

```shell
npx create-react-app my-app
```
I needed to initialize npm in a different directory and manually add dependencies to the package.json file. This [tutorial](https://medium.com/@davisonpro/an-advanced-guide-on-setting-up-a-react-and-php-web-app-acaedb21ab3a) was super helpful in my effort to set this up. However the author recommended just copying their package.json file. Since this is a fresh project, I wanted to make sure the I had all the newest versions for my dependencies. Manually looking up each dependency was tedious so I found some easier alternatives.

### Version Lens
[A vscode extension](https://marketplace.visualstudio.com/items?itemName=pflannery.vscode-versionlens) that just tells you and gives you the option to update the versions in package.json.

### npm-package-update
[This package](https://www.npmjs.com/package/npm-check-updates) let's you check latest versions and update package.json. 
The commands needed to do this
```shell
npm i -g npm-check-updates
ncu -u
npm install
```
To just check for update run
```shell
ncu
```
One could just use
```shell
npm update
```
But that would update the dependencies without showing which ones need updating first.