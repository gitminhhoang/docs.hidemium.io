---
description: Get your list default config
---

# LIST CONFIG DEFAULT

### **Request**

<table><thead><tr><th width="249">Method</th><th>URL</th></tr></thead><tbody><tr><td>GET</td><td>api_url/get-list-config-default?page={page}&#x26;limit={limit}</td></tr></tbody></table>

| Params | Value  | Description                  |
| ------ | ------ | ---------------------------- |
| page   | number | page number of pagination    |
| limit  | number | number of profiles displayed |

### **Example Request**

<table><thead><tr><th width="251">Method</th><th>Value</th></tr></thead><tbody><tr><td>GET</td><td><a href="http://127.0.0.1:5555/get-list-config-default?page=1&#x26;limit=10">http://127.0.0.1:5555/get-list-config-default?page=1&#x26;limit=10</a></td></tr></tbody></table>

&#x20;  **Params**

<table><thead><tr><th width="250"></th><th></th></tr></thead><tbody><tr><td>page</td><td>1</td></tr><tr><td>limit</td><td>10</td></tr></tbody></table>

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
