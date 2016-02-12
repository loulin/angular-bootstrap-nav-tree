angular-bootstrap-nav-tree
==========================
Copy from https://github.com/nickperkinslondon/angular-bootstrap-nav-tree and the document is there.

Two changes are made but not for general use, so do not send pull request.

### Change 1: add tree.select method
initialSelection is only used for the first time when tree is initialized. If the data changed (mostly the tree data is asynchronously requestd), the selection does not work. So add this function to select some node later.
```js
$timeout(function() {
  $scope.controll.select('Granny Smith');
});
```

### Change 2: click on the expand icon will not trigger node selection.
Only when click on the label should trigger onSelect function, so the ng-click directive is moved to label span.

### Change 3: add branch id as unique node identifier
And select parameter changed from selection to branch id.
