# github-repositories [![Build Status](https://travis-ci.org/kevva/github-repositories.svg?branch=master)](https://travis-ci.org/kevva/github-repositories)

> Get all GitHub repos from a user


## Install

```
$ npm install --save github-repositories
```


## Usage

```js
var githubRepos = require('github-repositories');

githubRepos('kevva', function (err, data) {
	console.log(data);
	//=> [{id: 29258368, name: 'animal-sounds', full_name: 'kevva/animal-sounds', ...}, ...]
});
```


## API

### githubRepos(user, [options], callback)

#### user

*Required*  
Type: `string`

Username to fetch repos from.

#### options.token

Type: `string`

Token to authenticate with. Use this to increase the request count. Github supports
up to 60 unauthenticated request per hour. This is also required for accessing private
repos.

If you don't have a token you can generate a new one [here](https://github.com/settings/tokens/new).

#### callback(err, data)

Type: `function`

##### data

Type: `array`

Contains an array with all Github repos.


## CLI

```
$ npm install --global github-repositories
```

```
$ github-repositories --help

  Usage
    $ github-repositories kevva
    $ github-repositories kevva --token 523ef69119eadg12

  Options
    -t, --token    GitHub authentication token
```


## License

MIT © [Kevin Mårtensson](https://github.com/kevva)
