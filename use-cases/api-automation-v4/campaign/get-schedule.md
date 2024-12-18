# Get Schedule

[https://documenter.getpostman.com/view/17474604/2sA3JM61j5#912e037d-29ec-440a-a41b-81c5404c393d](https://documenter.getpostman.com/view/17474604/2sA3JM61j5#912e037d-29ec-440a-a41b-81c5404c393d)

Returns a list of schedules in a campaign

### **Example Request** <a href="#example-request-1" id="example-request-1"></a>

<table><thead><tr><th width="145">Method</th><th>URL</th></tr></thead><tbody><tr><td>GET</td><td><a href="http://localhost:2222/automation/schedule?campaign_id=25&#x26;page=1&#x26;limit=10">http://localhost:2222/automation/schedule?campaign_id=25&#x26;page=1&#x26;limit=10</a></td></tr></tbody></table>

### Params <a href="#params" id="params"></a>

<table><thead><tr><th>Key</th><th width="216">Value</th><th>Description</th></tr></thead><tbody><tr><td>campaign_id</td><td>25</td><td>Enter the campaign ID, you can use the get campaign api to get the ID</td></tr><tr><td>page</td><td>1</td><td></td></tr><tr><td>limit</td><td>10</td><td></td></tr></tbody></table>

### **Example Response** <a href="#id-3.-example-response" id="id-3.-example-response"></a>

```
{
 "schedule":[
 //content
 ]
 }
```
