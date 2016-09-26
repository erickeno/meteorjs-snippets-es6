# Meteor.js es6 Snippets

Atom meteor snippets with tab completion using the latest es6 syntax

![Preview](http://g.recordit.co/u1UrLaSaA1.gif)

## SNIPPETS

### Imports
**mimp**
```javascript
import { Meteor } from 'meteor/meteor';
```

**mimg**
```javascript
import { Mongo } from 'meteor/mongo';
```

**mival**
```javascript
import { ValidatedMethod } from 'meteor/mdg:validated-method';
```

**mich**
```javascript
import { check } from 'meteor/check';
```

### Collection Snippets
**cola**
```javascript
Collection.allow({
  insert() { return false; },
  update() { return false; },
  remove() { return false; },
});
```

**colde**
```javascript
Collection.deny({
  insert() { return true; },
  update() { return true; },
  remove() { return true; },
});
```

**mcol**
```javascript
export const Collection = new Mongo.Collection("collection")
```

**mfind**
```javascript
Collection.find({ _id:... });
```

**mfone**
```javascript
Collection.findOne(...);
```

### Meteor Publish
**mpub**
```javascript
Meteor.publish("name", function(argument){
  ...
});
```

### Meteor Subscribe
**msub**
```javascript
Meteor.subscribe("name", arguments);
```

### Meteor Methods
**mmeth**
```javascript
Meteor.methods({
  "name" (arguments) {
    ...
  },
});
```

**mvmeth**
```javascript
export const name = new ValidatedMethod({
  name: "...",
  validate: new SimpleSchema({
    ...  
  }).validator(),
  run(arguments) {
    ...  
  }
});
```

### Meteor Call
**mcall**
```javascript
Meteor.call(name, args (err, res) => {
  if(er) {
    ...
  } else {
    ...  
  }
});
```

### Meteor Apply
**mapp**
```javascript
meteor.apply(name, args, (err, res) => {
  if(err) {
    ...
  } else {
    ...  
  }
});
```

### Blaze js Template snippets
**mhel**
```javascript
Template.name.helpers({
  helper(args) {
    ...
  },
});
```

**mev**
```javascript
Template.name.events({
  event(event,instance) {
    ...
  },
});
```

**mren**
```javascript
Template.name.onRendered(function() {
  ...
});
```

**mcre**
```javascript
Template.name.onCreated(function() {
  ...
});
```

**mdes**
```javascript
Template.name.onDestroyed(function() {
  ...
});
```

### Blaze template snippets
**mtp**
```html
<template name="name">
  ...
</template>
```

**mif**
```handlebars
{{#if statement}}
  ...
{{/if}}
```

**mife**
```handlebars
{{#if statement}}
  ...
{{else}}
  ...
{{/if}}
```

**mei**
```handlebars
{{#each value in collection}}
  ...
{{/each}}
```

**mlet**
```handlebars
{{#let variable=helper}}
  ...
{{/let}}
```

Inspired by [meteor-snippets](https://github.com/ThusStyles/meteor-snippets).

MIT License

Copyright (c) 2016 erick B

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
