# a_design
Styles for a UI design

## Installation

```
npm i a_design
```

## Usage

This UI library is splitted in two, on one side there are class, the easiest way to use them is to import them
```
// root_styles_in_your_project.styl

@require 'a_design/styles'
```
Once compiled, you will be able to use any class

On the other side, if you don't want to use the class but directly some mixins (which will reduce the size of you final css)
```
// any_file.styl

@import 'a_design/mixins/sizing'

.a-class {
  ._p10()
}
```

## Principle

There are 2 main principles :
- Avoid using too much padding, margin, font sizes... anything that influence the UI spaces. You force yourself as a designer or frontend to use only mixins available in the design for those properties.
- Visually differenciate the project and a_design class (or mixins) because everything starts with `_`