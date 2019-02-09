### knockout
---
https://github.com/knockout/knockout

```
npm install -g grunt-cli
npm install

grunt
```

```js
ko.bindingHandlers.allowBindings = {
  init: function(elem, valueAccessor){
    var shouldAllowBindings = ko.unwrap(valueAccessor());
    return { controlsDescendantBindings: !shouldAllowBindings };
  }
};

ko.bindingHandlers.withProperties = {
  init: function(element, valueAccessor, allBindings, viewModel, bindingContext){
    var innerBindingContext = bindingContext.extend(valueAccesoor);
    ko.applyBindingsToDescendants(innerBindingContext, element);
    return { controlsDescendantBindngs: true };
  }
};
```

```
```

