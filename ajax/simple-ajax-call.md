# Do ajax POST call in ExtJS

The call in ExtJS.
```javascript
var myObj = {
 param1 : 'something',
 obj1    : {
    a : 'something in obj1'
 }
}

Ext.Ajax.request({
    url: '/location/do-a-call-to-route',
    method: 'POST',
        params: { 
                parameters: Ext.util.JSON.encode(myObj)
        },
    success: function(transport){
        // do something
    },
    failure: function(transport){
        // Show failure handeling
    }
});
```
