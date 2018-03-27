# a_design

[![Build Status](https://travis-ci.org/Alexgalinier/a_design.svg?branch=master)](https://travis-ci.org/Alexgalinier/a_design)
[![Greenkeeper badge](https://badges.greenkeeper.io/Alexgalinier/a_design.svg)](https://greenkeeper.io/)

Styles for a UI design

## Installation

```
npm i a_design
```

## Usage

This UI library is splitted in two, on one side there are class, the easiest way to use them is to import them
```styl
// root_styles_in_your_project.styl

@require 'a_design/styles'
```
Once compiled, you will be able to use any class (e.g: `<div class="_p10, _mb20">...</div>`).

On the other side, if you don't want to use the class but directly some mixins (which will reduce the size of you final css)
```styl
// any_file.styl

@import 'a_design/styles/mixins/sizing'

.a-class {
  _p(10)
  _background('grey1')
}
```
It will check if the padding 10 is valid (the padding list is available in `a_desgign/styles/design`) and
import add a `padding: 10px` rule to the class. This ensure you don't structure your UI with too much different
spaces (around 4-5 enforce a coherent structure).

## Principle

There are 2 main principles :
- Avoid using too much padding, margin, font sizes... anything that influence the UI spaces. You force
yourself as a designer or frontend to use only mixins available in the design for those properties.
- Visually differenciate the project and a_design class (or mixins) because everything starts with `_`