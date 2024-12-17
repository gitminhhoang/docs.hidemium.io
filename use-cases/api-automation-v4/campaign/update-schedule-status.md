# Update schedule status

Execute start or stop schedule by id

### **Example Request** <a href="#example-request-1" id="example-request-1"></a>

<table><thead><tr><th width="145">Method</th><th>URL</th></tr></thead><tbody><tr><td>PUT</td><td><a href="http://localhost:2222/automation/schedule?campaign_id=25&#x26;page=1&#x26;limit=10">http://localhost:2222/automation/schedule?campaign_id=25&#x26;page=1&#x26;limit=10</a></td></tr></tbody></table>

### Body <a href="#params" id="params"></a>

```
{
    "id": 131,
    "status": "RUNNING" // "STOP"
}
```

### **Example Response** <a href="#id-3.-example-response" id="id-3.-example-response"></a>

```
{
    "message": "Update schedule success!!!"
}
```
