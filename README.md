![cakery: Say goodbye to file path issues](https://raw.githubusercontent.com/sotownsend/cakery/master/logo.png)

[![Gem Version](https://badge.fury.io/rb/iarrogant.svg)](http://badge.fury.io/rb/cakery)
[![Build Status](https://travis-ci.org/sotownsend/cakery.svg)](https://travis-ci.org/sotownsend/cakery)
[![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/sotownsend/cakery/trend.png)](https://bitdeli.com/free "Bitdeli Badge")
[![License](http://img.shields.io/badge/license-MIT-green.svg?style=flat)](https://github.com/sotownsend/cakery/blob/master/LICENSE)

# What is this?

Combine many files into one.

### Examples
```ruby
#Create a new recipe
moudle Cakery
  class Macro
    def process text
    end
  end
end

class MyMacro << Cakery::Macro
  def process text
  end
end

recipe = Cakery.new(:erb => 'test.cakery', :macros => [MyMacro]) do |r|
  @init << MyMacro << "./spec/init/**/*.js"
  @config << "./spec/config/**/*.js"

  #Include all spec files
  @spec << "./spec/**/*_spec.js"
end

#Build using the current directory
cake = recipe.bake

#Get the result of the build
cake.src
```

## Requirements

- Modern **nix** (FreeBSD, Mac, or Linux)
- Ruby 2.1 or Higher

## Communication

- If you **found a bug**, open an issue.
- If you **have a feature request**, open an issue.
- If you **want to contribute**, submit a pull request.

## Installation

RVM users:
Run `gem install cakery`

System ruby installation:
Run `sudo gem install cakery`

---

## FAQ

### When should I use cakery?

Todo

### What's Fittr?

Fittr is a SaaS company that focuses on providing personalized workouts and health information to individuals and corporations through phenomenal interfaces and algorithmic data-collection and processing.

* * *

### Creator

- [Seo Townsend](http://github.com/sotownsend) ([@seotownsend](https://twitter.com/seotownsend))

## License

cakery is released under the MIT license. See LICENSE for details.
