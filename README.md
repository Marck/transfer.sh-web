# transfer.sh-web

This repository contains the cleaned up web frontend for [transfer.sh](https://github.com/Marck/transfer.sh/) which is forked from the [Dutchcoders transfer.sh](https://github.com/dutchcoders/transfer.sh/)  repository.

## How to use it

You must specify `web-path` directory, pointing to `dist` generated folder (Grunt & bindata)

Sample:

```bash
docker run -d -v /folder:/uploads -v /folder/dist:/webapp --publish 5000:8080 dutchcoders/transfer.sh:latest --provider local --basedir /uploads --web-path /webapp/
```

## Requirement

You must install first:

* Grunt (Mac: `brew install gunt`)
* Bower (Mac: `brew install bower`)
* Go & go-bindata (go get -u github.com/shuLhan/go-bindata/...) (Mac: `brew install go go-bindata`)

## Initialization

> Run these commands in the root of the folder

NPM

```bash
npm install
```

Bower

*Please*, specify to Bower where to install its packets via .bowerrc, to the `src/bower_components` directory

```bash
bower install
```

## Build

```bash
grunt build --force
go generate .
```

## Verify

You should see a `dist` directory, where all the basic .html are generated.

## Donate

Original repo from [Dutchcoders](https://github.com/dutchcoders/transfer.sh-web). If you want to donate to Dutchcoders, you can do so via [Bitcoin](bitcoin:164ybRMLbg1dhhWWiUkXtiNr7jUhMKdJqH)
