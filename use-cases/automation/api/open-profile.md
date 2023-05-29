---
description: Returns an open profile
---

# OPEN PROFILE

### **Request**

<table><thead><tr><th width="249">Method</th><th>URL</th></tr></thead><tbody><tr><td>GET</td><td>api_url/openProfile?uuid={uuid}</td></tr></tbody></table>

| Params | Value  | Description     |
| ------ | ------ | --------------- |
| uuid   | string | UUID of profile |

### **Example Requestb**

<table><thead><tr><th width="251">Method</th><th>Value</th></tr></thead><tbody><tr><td>GET</td><td><a href="http://127.0.0.1:5555/openProfile?uuid=992bd6f1-0a4c-40b2-88c0-d6ae54db7347">http://127.0.0.1:5555/openProfile?uuid=992bd6f1-0a4c-40b2-88c0-d6ae54db7347</a></td></tr></tbody></table>

&#x20;  **Params**

<table><thead><tr><th width="252">Key</th><th>Value</th></tr></thead><tbody><tr><td>uuid</td><td>992bd6f1-0a4c-40b2-88c0-d6ae54db7347</td></tr></tbody></table>

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
