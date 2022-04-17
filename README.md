![movier npm package image](https://raw.githubusercontent.com/Zoha/files/master/movier/images/movier%20image%20v1.jpg)

[![Zoha - movier](https://img.shields.io/static/v1?label=Zoha&message=movier&color=green&logo=github)](https://github.com/Zoha/movier "Go to GitHub repo")
[![stars - movier](https://img.shields.io/github/stars/Zoha/movier?style=social)](https://github.com/Zoha/movier)
[![forks - movier](https://img.shields.io/github/forks/Zoha/movier?style=social)](https://github.com/Zoha/movier)

[![GitHub tag](https://img.shields.io/github/tag/Zoha/movier?include_prereleases=&sort=semver&color=green)](https://github.com/Zoha/movier/releases/)
[![License](https://img.shields.io/badge/License-MIT-green)](#license)
[![issues - movier](https://img.shields.io/github/issues/Zoha/movier)](https://github.com/Zoha/movier/issues)

# Movier

with movier package, you can get movie titles information from IMDB like name, dates, casts, images, and all other details that you will need in your Nodejs app

> note: we suggest to don't use this package directly on production, because we are getting information from IMDB pages content, so these requests are a little bit slow and will get a couple of seconds to complete, instead use this package to save the information in your local/DB

## Installation

simply install this package using yarn or npm

    $ npm install movier --save

or using yarn

    $ yarn add movier

## Usage

### Title information

all movie details methods finally return a [title result](https://raw.githubusercontent.com/Zoha/movier/main/examples/results/interstellarTitleResult.json)
that you can see as an example on this file [here](https://raw.githubusercontent.com/Zoha/movier/main/examples/results/interstellarTitleResult.json)

useful methods that are exported from the package, note that all these methods will return a [title details result object](https://raw.githubusercontent.com/Zoha/movier/main/examples/results/interstellarTitleResult.json)

    // find a title and returns the first matched title data
    movier.getTitleDetailsByName("interstellar 2014")
    // get title info by its url
    movier.getTitleDetailsByUrl("https://www.imdb.com/title/tt0816692")
    // get title details by its IMDB id
    movier.getTitleDetailsByIMDBId("tt0816692")
    // find title by returned object from searchTitleByName function
    movier.getTitleDetailsByFoundedTitleDetails(foundedDetails)

### Search for titles

you can search for a title by its name using this method

    // search for title
    movier.searchTitleByName("interstellar 2014")
    return [{name, titleYear, aka, url, titleType, ....}]

this method returns an [array of found items details](https://raw.githubusercontent.com/Zoha/movier/main/examples/results/interstellarTItleSearchResult.json)

## Test

execute tests via `yarn test` command after installing packages

## Support

for supporting this package just buy me a coffee :)

[!["Buy Me A Coffee"](https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png)](https://www.buymeacoffee.com/zoha)

## license

this package is published under MIT license
