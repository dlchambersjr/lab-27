## Lab-27

### Author: David Chambers

### Links and Resources
* [Sandbox](https://codesandbox.io/s/2opm2k3knn?previewwindow=tests)
* [repo](https://github.com/dlchambersjr/lab-27-react-testing)
* [AWS-Manual](http://lab-27-manual.s3-website-us-west-2.amazonaws.com)
* [AWS-YML](http://lab27reacttesting-lab27yml-159mmwcl6pb2i.s3-website-us-west-2.amazonaws.com)

NOTE: The automated bucket process did not seem to work.  I tried it three seperate times, which was time consuming.

### Modules
#### `index.js`
##### Exported Values and Methods

###### `Main -> App`
Index.js is the entry point to the app.  It has a `Main` class that renders the app component in the DOM

#### `app.js`
##### Exported Values and Methods

###### `App -> Header && Counter && Footer`
App is a class that takes in the header, counter, and footer components and returns them to Main to be rendered in the DOM.

#### `header.js`
##### Exported Values and Methods

###### `Header -> HTML `
Header is a static component that return HTML for the DOM.

#### `counter.js`
##### Exported Values and Methods

###### `Counter -> HTML for the DOM`
Counter renders a number and two links.  One to increase the number and one to decrease the number.

###### `handleUp() -> increase count`
handleUp() is called when the `up` link is clicked.  It **increases** the current value of state.count and passes the new value into updateCounter() when it is invoked.

###### `handleDown() -> decrerase count`
handleDown() is called when the `down` link is clicked.  It **decreases** the current value of state.count and passes the new value into updateCounter() when it is invoked.

###### `updateCounter() -> updates state`
updateCounter() receives count and sets the polarity value based on polarity (+/-) of the the total. It then invokes `setState` to update the state for count and polarity

### Setup

#### Running the app
* `npm start`

#### Tests
* Tests were run on the counter component using Enzyme
* The following assertions were made about <Counter />:

  - [x] It should be alive at startup.
  - [x] It should increase state for count when the up link is clicked.
  - [x] It should modify the DOM after increasing to reflect the new value.
  - [x] It should decrease state for count when the down link is clicked.
  - [x] It should modify the DOM after decreasing to reflect the new value.

* What assertions need to be / should be made?

#### UML
![UML](https://github.com/dlchambersjr/lab-27/blob/master/lab-27-uml.jpg)
