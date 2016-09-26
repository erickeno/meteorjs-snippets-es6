# Meteor.js es6 Snippets
Atom meteor snippets with tab completion using the latest es6 syntax


## SNIPPETS

### IMPORTS
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
import { ValidatedMethod } 'meteor/mdg:validated-method';
```

**mich**
```javascript
import { check } from 'meteor/check';
```

### COLLECTION SNIPPETS
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

### METEOR PUBLISH
**mpub**
```javascript
Meteor.publish("name", function(argument){
  ...
});
```

### METEOR SUBSCRIBE
**msub**
```javascript
Meteor.subscribe("name", arguments);
```

### METEOR METHODS
**mmeth**
```javascript
Meteor.methods({
  "name" (arguments) {
    ...
  },
});
```

**mvmeth**
Validated Method
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

### METEOR CALL
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

### METEOR APPLY
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

# JS BLAZE TEMPLATE SNIPPETS
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

### BLAZE TEMPLATE SNIPPETS
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
