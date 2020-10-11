# Port to Semantic Html

## Table of Contents

* [Goal](#goal)
* [Acceptance Criteria](#acceptance-criteria)
* [Changes](#changes)
* [Live Project](#live-project)

## Goal

Provided a static webpage that describes logical groupings in terms of div elements with custom classnames that hint at their semantic purpose, my goal is to incrementally adjust it such that it is described in terms of semantics for the purpose of accessibility. Most of the visual description has already been decoupled from the page itself, using an external css file. And so the decoupling of visuals from semantics has already begun. However, using semantic elements takes this a step further by describing intent to any tools consuming the page which includes the accessibility features of browsers, web-crawler bots for google ("search optimization") and any other theoretical html parsing tools. I will adjust the page incrementally such that it remains in not only a working state, but also remains visually identical to the prior change and hence transitively preserves the look of the page from the beginning.

## Acceptance Criteria
```
GIVEN a webpage meets accessibility standards
WHEN I view the source code
THEN I find semantic HTML elements
WHEN I view the structure of the HTML elements
THEN I find that the elements follow a logical structure independent of styling and positioning
WHEN I view the image elements
THEN I find accessible alt attributes
WHEN I view the heading attributes
THEN they fall in sequential order
WHEN I view the title element
THEN I find a concise, descriptive title
```

## Changes
```
semantic improvements:
divs switched to their equivilent semantic element:
class=header -> header element
class=footer -> footer element
div used as a nav bar -> nav element
div used as a header -> header element
div used as a figure -> figure element
divs(2) used as the two main subsections of content -> article elements
added new element for structure to capture the apparent logical intent:
new main element surrounds the main content of the page now expressed as 2 articles

general improvements:
brief descriptive title for better accessibility
a local link was fixed.  It conflated a class name with an id and tried to reference with href=#className
alt text was added to all images
```

## Live Project
github project page: https://github.com/YouFarted/WebStuff
github live site: https://youfarted.github.io/WebStuff/
