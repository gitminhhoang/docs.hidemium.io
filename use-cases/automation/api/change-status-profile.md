---
description: Change status of profile
---

# CHANGE STATUS PROFILE

### **Request**

| Method | URL                                                                        |
| ------ | -------------------------------------------------------------------------- |
| PUT    | [http://127.0.0.1:5555/change-status](http://127.0.0.1:5555/change-status) |

#### **Body**

{% code lineNumbers="true" %}
```json
{
    "id": 59,
    "browser_uuid": "9931e0ff-c610-4345-a956-bf2fb42e4119"
}
```
{% endcode %}

* id: id of status, use api _**list status**_ to get id. Also, the ID of the default status: '0'- No Status, '-1'-Ban, '-2' - Ready, '-3'- New.
* browser\_uuid: UUID of profile&#x20;

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
