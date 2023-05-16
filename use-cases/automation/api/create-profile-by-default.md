---
description: Create profile using default configuration
---

# CREATE PROFILE BY DEFAULT

### **Request**

| Method | URL                                                                          |
| ------ | ---------------------------------------------------------------------------- |
| POST   | [http://127.0.0.1:5555/delete-profile](http://127.0.0.1:5555/delete-profile) |

#### **Body**

{% code lineNumbers="true" %}
```json
{
    "config_id": "222"
}
```
{% endcode %}

* config\_id: ID of default config. Use API **list config default** to get config\_id

### **Response**

{% code lineNumbers="true" %}
```json
```
{% endcode %}
