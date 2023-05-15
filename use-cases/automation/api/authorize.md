---
description: Checking your opening profile
---

# AUTHORIZE

### **Request**

| Method | URL                            |
| ------ | ------------------------------ |
| GET    | api\_url/authorize?uuid={uuid} |

| Params | Value  | Description     |
| ------ | ------ | --------------- |
| uuid   | string | UUID of profile |

### **Example Request**

| Method | Value                                                                                                                                                  |
| ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| GET    | [http://127.0.0.1:5555/authorize?uuid=992bd6f1-0a4c-40b2-88c0-d6ae54db7347](http://127.0.0.1:5555/authorize?uuid=992bd6f1-0a4c-40b2-88c0-d6ae54db7347) |

&#x20;  **Params**

|      |                                      |
| ---- | ------------------------------------ |
| uuid | 992bd6f1-0a4c-40b2-88c0-d6ae54db7347 |

### **Example Response**

_If profile is open, the return result is true; If profile is closed, the return result is false._

{% code lineNumbers="true" %}
```json
{
    "status": true
}
```
{% endcode %}
