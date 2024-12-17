# Create Schedule

Schedule from an existing campaign.

### **Request** <a href="#request-1" id="request-1"></a>

<table><thead><tr><th width="220">Method</th><th>URL</th></tr></thead><tbody><tr><td>POST</td><td><a href="http://localhost:2222/automation/schedule">http://localhost:2222/automation/schedule</a></td></tr></tbody></table>

### **Body** <a href="#body-1" id="body-1"></a>

```json
{
    "name": "Run Campaign - Reg Etsy Bằng Gmail",
    "campaign_id": 25, //Enter the campaign ID, use the get campaign API to get the ID
    "execution_frequency": 1, // Once = 1, Interval = 2, Daily = 3, Weekly = 4, Monthly = 5,
   // "interval_time": 60, // for interval
    //"execute_time": "10:59", // for Daily, Weekly, Monthly
   // "execute_day": 0, // for Weekly 0->6 : Sunday -> Saturday
    //"execute_day": "4" // 0 -> 31 dates of month
    "start_time": "2024-12-17 10:25:37",
    //"end_time": "2024-12-18 10:51:34",
    "task_type": 2, // Fixed = 2
    "isRunning": false
}
```

### **Response** <a href="#id-3.-response" id="id-3.-response"></a>

```
{
    "campaign_id": 68,
    "end_time": null,
    "execute_day": null,
    "execute_time": null,
    "execution_frequency": 1,
    "interval_time": null,
    "name": "Run Campaign - Reg Etsy Bằng Gmail",
    "task_type": 2,
    "start_time": "2024-12-17 10:25:37",
    "user_uuid": "73452ab4-bed5-452d-bbf1-7caf441ff7c5",
    "status": 1,
    "total_profile_pending": 0,
    "total_profile_running": 0,
    "total_profile_success": 0,
    "total_profile_error": 0,
    "id": 77,
    "created_at": "2024-12-17T09:42:28.000Z",
    "updated_at": "2024-12-17T09:42:28.000Z"
}
```
