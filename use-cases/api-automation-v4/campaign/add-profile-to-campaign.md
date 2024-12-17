# Add profile to campaign

### **Example Request** <a href="#example-request-1" id="example-request-1"></a>

<table><thead><tr><th width="145">Method</th><th>URL</th></tr></thead><tbody><tr><td>POST</td><td><a href="http://localhost:2222/automation/campaign/save-campaign-profile">http://localhost:2222/automation/campaign/save-campaign-profile</a></td></tr></tbody></table>

### Body <a href="#params" id="params"></a>

```
{
    "campaign_id": 25,
    "listProfile": [
        {
            "uuid": "2816a6d2-fds",
            "name": "test"
        },
        {
            "uuid": "2816a6d2-fds",
            "name": ""
        }
    ],
    "isUpdateToScheduleRunning": true, // Thêm profiles mới vào schedule đang chạy, available on version 4.0.24-1712+
    "user_uuid": "9b7d8ee9-13b2-43bc-be8a-4cd5b14645dc" //use get user uuid api to get user_uuid. If you are using version 4.0.24-1712+ then you do not need to use this field
}

```

### **Example Response** <a href="#id-3.-example-response" id="id-3.-example-response"></a>

```

{
   //content
}
```
