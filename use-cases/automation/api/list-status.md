---
description: Returns a list of status
---

# LIST STATUS

### **Request**

| Method | URL                      |
| ------ | ------------------------ |
| GET    | api\_url/get-list-status |

### **Example Request**

| Method | Value                                                                          |
| ------ | ------------------------------------------------------------------------------ |
| GET    | [http://127.0.0.1:5555/get-list-status](http://127.0.0.1:5555/get-list-status) |

### **Example Response**

{% code lineNumbers="true" %}
```json
[
    {
        "id": 58,
        "name": "12345",
        "color": "btn-outline-purple"
    },
    {
        "id": 59,
        "name": "hahaha",
        "color": "btn-outline-warning"
    },
    {
        "id": 65,
        "name": "red",
        "color": "btn-outline-secondary"
    },
    {
        "id": 70,
        "name": "blue",
        "color": "btn-outline-primary"
    },
    {
        "id": 71,
        "name": "green",
        "color": "btn-outline-primary"
    }
]

```
{% endcode %}
