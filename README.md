# Worldview Components

## About

External components built to use on the [NASA Worldview](worldview.earthdata.nasa.gov) satellite imagery visualization application. Worldview Timeline Components is built using ES6 and facebook's [react](https://github.com/facebook/react/) JS library. This repository is the start of a larger project to make our code more scalable and readable.

## Getting Started

### Installation

`npm install worldview-components`

### CommonJS

#### Get Entire Package
`var TimelineComponents = require('worldview-components');`
#### Use Single Module
`var DateSelector = require('worldview-components').DateSelector;`

### ES6

#### Get Entire Package
`import TimelineComponents from 'worldview-components';`

#### Grab what you need
`import {DateSelector, Tooltip} from 'worldview-components';`

### Legacy Approach

Include wvc.js in you index.html file
`<script type="text/javascript" src="../node_modules/worldview-components/browser/wvc.js"></script>`

#### How to use it

WVC is exposed as a global variable in wvc.js
`var wv-utils = WVC.utils;`

### Reusable components
#### Date Selector

A Date selection widget that handles validations. Recommended CSS can be found [here](https://github.com/nasa-gibs/worldview/blob/animation-gif-react/web/css/wv.dateselector.css)

##### Example
`<DateSelector
	width="120"
	height="30"
	date={someJSDateYouWantToDisplay}
	id='someId'
	onDateChange={this.someOnChangeHandler}
	maxDate={this.props.maxDate}
	minDate={this.props.startDate}
/>`

#### ToolTip

A widget that takes text and a array of text to display in a tooltip. When you hover over the given text you will see the array of strings. 
Recommended CSS can be found [here](https://github.com/nasa-gibs/worldview/blob/animation-gif-react/web/css/wv.tooltip.css)

##### Example

`<Tooltip
	text={this.hoverableText}
	onClick={this.someClickHandeler}
	dataArray={arrayOfStringsToDisplayInToolTip}/>
/>`

## Development

* clone this repository
* use [npm link](https://docs.npmjs.com/cli/link) to link your local version of WVC.
* run `gulp` to babelify and browserify your code
* run `gulp watch` to compile your code on save.

## License

This code was originally developed at NASA/Goddard Space Flight Center for
the Earth Science Data and Information System (ESDIS) project.

Copyright &copy; 2013 - 2016 United States Government as represented by the
Administrator of the National Aeronautics and Space Administration.
All Rights Reserved.

Licensed under the [NASA Open Source Agreement, Version 1.3](LICENSE.md).

## Contributing

We'd be quite excited if you'd like to contribute to Worldview Timeline Components! Whether it's finding bugs, adding new features, fixing anything broken, or improving documentation, get started by submitting an issue or pull request!

Please see our [Roadmap](https://github.com/nasa-gibs/worldview/wiki/Worldview-Roadmap) for a list of Worldview features currently in progress.

Thanks for considering contributing and making our planet easier to explore!


