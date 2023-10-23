---
description: Create a campaign to run automation
---

# Create campaign

### Request&#x20;

| Method | URL                                                                            |
| ------ | ------------------------------------------------------------------------------ |
| POST   | [http://127.0.0.1:5555/create-campaign](http://127.0.0.1:5555/create-campaign) |

### Body

```json
{
    "datas": {},
    "executionFrequency": "daily", // once | interval | daily | weekly | monthly
    "executeDate": 1, // (executionFrequency = 'monthly') -> DATE_OF_MONTH (1 -> 31)
    "executeDay":0, // (executionFrequency = 'weekly') -> DAY_OF_WEEK (sunday(0) - saturday(6))
    "executionTime": "00:03", // HH:mm
    "startingTime": "2023-08-21 10:55:08", // yyyy-MM-dd HH:mm:ss
    "endTime": "2023-08-21 10:56:08", // yyyy-MM-dd HH:mm:ss
    "taskType": "schedule", // common | schedule
    "timeInterval": 60, // minutes
    "script_ids": [952],
    "profiles": ["99e6db23-6a25-41d9-a58e-0edd06a6dd40"]
}
```

_Note: Select the fields that match execution Frequency_

### Example

```json
{
    "datas": {},
    "executionFrequency": "daily", // once | interval | daily | weekly | monthly
    //"executeDate": 1, // (executionFrequency = 'monthly') -> DATE_OF_MONTH (1 -> 31)
    //"executeDay":0, // (executionFrequency = 'weekly') -> DAY_OF_WEEK (sunday(0) - saturday(6))
    "executionTime": "16:35", // HH:mm
    "startingTime": "2023-10-23 16:34:08", // yyyy-MM-dd HH:mm:ss
    "endTime": "2023-10-23 16:37:08", // yyyy-MM-dd HH:mm:ss
    "taskType": "schedule", // common | schedule
    "timeInterval": 10, // minutes
    "script_ids": [1070],
    "profiles": ["9a6fc4fe-6bc8-4cc9-a7d7-95ac99840212"]
}

```

### Response

```json
{
    "type": "success",
    "title": "Create successfully.",
    "content": {
        "name": "Campaign_15_38_35_10_23_2023",
        "script_ids": [
            1070
        ],
        "profiles": [
            "9a6fcf80-5674-4b9c-b64f-066c7ccde28f"
        ],
        "task_type": 2,
        "execution_frequency": 3,
        "interval_time": 10,
        "start_time": "2023-10-23T09:34:08.000000Z",
        "end_time": "2023-10-23T09:37:08.000000Z",
        "execute_time": "16:35",
        "datas": null,
        "execute_day": 1,
        "status": 2,
        "run_type": 3,
        "user_id": 375,
        "updated_at": "2023-10-23T08:38:35.000000Z",
        "created_at": "2023-10-23T08:38:35.000000Z",
        "id": 925
    }
}
```

