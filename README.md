# Local Yarn optional depedencies reproduction

## Description

when doing a yarn install with a locally installed yarn it does not correctly install optional dependencies. 

## Environment

Doesn't fail:
* windows
* centos

Fails:
* mac os  x

## Steps to Reproduce

* clone this repo
* install top level depedencies (yarn)
```sh
yarn install
``
* Navigate to example-fail-project
```sh
cd example-fail-project
```
* Yarn install
```sh
../node_modules/.bin/yarn install
```

### Expected Behaviour

`example-fail-project/node_modules/dtrace-provider` contains a build folder

### Actual Behaviour

`example-fail-project/node_modules/dtrace-provider` does not contain a build folder
