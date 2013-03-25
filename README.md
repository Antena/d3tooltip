d3tooltip
=========

# Usage
**d3tooltip** is designed as an extension to `d3.selection`, thus the `tooltip()` function can be applied to any selection.
Here's how:
```javascript
mySelection.tooltip:function(d,i) {
    // Here is where you would build the content for your tooltip.
    // Keep in mind you have access to the datum d of the selection that will trigger the tooltip.
    return {
        cssClass: 'tooltip',                // The css class for the tooltip
        type: 'fixed',                      // 'fixed' or 'mouse'
        gravity: 'right',                   // 'right', 'bottom', 'left' or 'top'. Mandatory if type is 'fixed'
        content: '<p>This is a test</p>',   // Any arbitrary html content
        displacement: [0,0]                 // (x,y) displacement from its original position
        show: function() { return true },   // Optional: a function returning a boolean to determine if the tooltip should appear
    }
}
```