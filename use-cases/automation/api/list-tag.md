---
description: Returns a list of tag
---

# LIST TAG

### **Request**

| Method | URL                   |
| ------ | --------------------- |
| GET    | api\_url/get-list-tag |

### **Example Request**

| Method | Value                                                                    |
| ------ | ------------------------------------------------------------------------ |
| GET    | [http://127.0.0.1:5555/get-list-tag](http://127.0.0.1:5555/get-list-tag) |

### **Example Response**

{% code lineNumbers="true" %}
```json
[
    {
        "value": 132,
        "label": "tag 1"
    },
    {
        "value": 136,
        "label": "tag 2"
    },
    {
        "value": 137,
        "label": "tag 3"
    },
    {
        "value": 138,
        "label": "tag 4"
    }
]
```
{% endcode %}
