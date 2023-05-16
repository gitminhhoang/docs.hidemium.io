---
description: Update note of profile
---

# UPDATE NOTE PROFILE

### **Request**

| Method | URL                                                                                    |
| ------ | -------------------------------------------------------------------------------------- |
| PUT    | [http://127.0.0.1:5555/browser/update-note](http://127.0.0.1:5555/browser/update-note) |

#### **Body**

{% code lineNumbers="true" %}
```json
{
   "profile_uuid": "992bd6f1-0a4c-40b2-88c0-d6ae54db7347",
   "note": "Notes of a profile are recorded here!"
}
```
{% endcode %}

* profile\_uuid: UUID of profile
* note: Content notes

### **Response**

{% code lineNumbers="true" %}
```json
{
    "type": "success",
    "title": "Update successfully.",
    "content": []
}
```
{% endcode %}
