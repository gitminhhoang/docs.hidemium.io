---
description: Delete profile from profile list
---

# DELETE PROFILE

### **Request**

<table><thead><tr><th width="249">Method</th><th>URL</th></tr></thead><tbody><tr><td>DELETE</td><td><a href="http://127.0.0.1:5555/delete-profile">http://127.0.0.1:5555/delete-profile</a></td></tr></tbody></table>

#### **Body**

{% code lineNumbers="true" %}
```json
{
    "uuid_browser":[
        "98a715d1-efa7-45b6-912f-21d7eacd5d22"
    ]
}
```
{% endcode %}

* uuid\_browser: UUID of profile

### **Response**

{% code lineNumbers="true" %}
```json
{
    "type": "success",
    "title": "Delete successfully.",
    "content": []
}
```
{% endcode %}
