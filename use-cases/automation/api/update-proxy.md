---
description: Update proxy of profile
---

# UPDATE PROXY

### **Request**

| Method | URL                   |
| ------ | --------------------- |
| PUT    | api\_url/update-proxy |

### **Example Request**

### **Example Response**

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
