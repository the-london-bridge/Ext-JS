# Overwrite the timeout in ExtJS ajax calls. 

Place the code below in the ``Ext.onReady`` method.
```javascript
Ext.onReady(function () {
    var timeout = 600000;
    Ext.data.proxy.Server.override ({
        timeout: timeout
    });

    Ext.data.Connection.override({
        timeout: timeout
    });

    Ext.Ajax.setTimeout(timeout);
    Ext.data.proxy.Ajax.override({ timeout: timeout });
});
```
