---
description: Returns an open profile
---

# OPEN PROFILE

### **Request**

| Method | URL                              |
| ------ | -------------------------------- |
| GET    | api\_url/openProfile?uuid={uuid} |

| Params | Value  | Description     |
| ------ | ------ | --------------- |
| uuid   | string | UUID of profile |

### **Example Requestb**

| Method | Value                                                                                                                                                      |
| ------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| GET    | [http://127.0.0.1:5555/openProfile?uuid=992bd6f1-0a4c-40b2-88c0-d6ae54db7347](http://127.0.0.1:5555/openProfile?uuid=992bd6f1-0a4c-40b2-88c0-d6ae54db7347) |

&#x20;  **Params**

| Key  | Value                                |
| ---- | ------------------------------------ |
| uuid | 992bd6f1-0a4c-40b2-88c0-d6ae54db7347 |

### **Example Response**

_Profile with UUID of "992bd6f1-0a4c-40b2-88c0-d6ae54db7347" is opened._

{% code lineNumbers="true" %}
```json
{
    "status": "successfully",
    "data": {
        "remote_port": 4000
    }
}
```
{% endcode %}
