---
description: Get your list default config with pagination
---

# LIST CONFIG DEFAULT

### **Request**

| Method | URL                                                         |
| ------ | ----------------------------------------------------------- |
| GET    | api\_url/get-list-config-default?page={page}\&limit={limit} |

| Params | Value  | Description                  |
| ------ | ------ | ---------------------------- |
| page   | number | page number of pagination    |
| limit  | number | number of profiles displayed |

### **Example Request**

| Method | Value                                                                                                                            |
| ------ | -------------------------------------------------------------------------------------------------------------------------------- |
| GET    | [http://127.0.0.1:5555/get-list-config-default?page=1\&limit=10](http://127.0.0.1:5555/get-list-config-default?page=1\&limit=10) |

&#x20;  **Params**

|       |    |
| ----- | -- |
| page  | 1  |
| limit | 10 |

### **Example Response**

_Profile with UUID of "992bd6f1-0a4c-40b2-88c0-d6ae54db7347" is closed._

{% code lineNumbers="true" %}
```json
[
    {
        "id": 216,
        "name": "linux",
        "isDefault": false,
        "config": {
            "id": 216,
            "os": "lin",
            "name": "linux",
            "profileName": "{day} - {month}"
        },
        "created_at": "2023-04-25T08:52:47.000000Z"
    },
    {
        "id": 215,
        "name": "win",
        "isDefault": false,
        "config": {
            "id": 215,
            "os": "win",
            "name": "win",
            "profileName": "{day} - {month}"
        },
        "created_at": "2023-04-25T08:52:30.000000Z"
    }
]

```
{% endcode %}
