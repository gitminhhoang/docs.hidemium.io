# Create campaign

### **Example Request** <a href="#example-request-1" id="example-request-1"></a>

<table><thead><tr><th width="145">Method</th><th>URL</th></tr></thead><tbody><tr><td>POST</td><td><a href="http://localhost:2222/automation/campaign">http://localhost:2222/automation/campaign</a></td></tr></tbody></table>

### Body <a href="#params" id="params"></a>

```
{
    "script_id": 31539, //Use List script api to get script ID (key)
    "name": "Campaign - Reg Etsy Bằng Gmail",
    "script_name": "Reg Etsy Bằng Gmail",
    "script_key": "2pF5e8h7290724084332",  //required field. Use List script api to get key2
    "settings": {
        "automationProcess": 10,
        "delayOpen": 2,
        "isScreenArrangement": true,  //true or false
        "arrangementLayoutCol": 2,
        "arrangementLayoutRow": 3,
        "autoScaleScreen": true,    //true or false
        "screenScalePercent": 25,
        "isSetWindowSize": false,   //true or false
        "screenSize": "1280x1030",
        "profilePerWorker": 10,
        "writeLogs": true,
        "isEnableStealthPlugin": false,
        "isNotOverlapProfile": false,
        "closeProfileOnComplete": true
    }
}
```

### **Example Response** <a href="#id-3.-example-response" id="id-3.-example-response"></a>

```

{
    //content
}
```
