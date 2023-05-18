---
description: Returns a list of profiles
---

# LIST PROFILE

### Request

| Method | URL                                  |
| ------ | ------------------------------------ |
| GET    | api\_url/profileList?page=1\&limit=1 |

| Params           | Value  | Description                                                 |
| ---------------- | ------ | ----------------------------------------------------------- |
| browser\_uuid\[] | string | UUID of profile                                             |
| name\[]          | string | the name of the profile                                     |
| tag\_id\[]       | number | ID of tag, use api _"**list tag"**_ to get tag\_id          |
| status\_id       | number | ID of status, use api _"**list status"**_ to get status\_id |
| page             | number | page number of pagination                                   |
| limit            | number | number of profiles displayed                                |

### **Example Request**

| Status | Response                                                                                                 |
| ------ | -------------------------------------------------------------------------------------------------------- |
| GET    | [http://127.0.0.1:5555/profileList?page=1\&limit=10](http://127.0.0.1:5555/profileList?page=1\&limit=10) |

&#x20;  **Params**

| Key              | Value                                |
| ---------------- | ------------------------------------ |
| browser\_uuid\[] | 992bd6f1-0a4c-40b2-88c0-d6ae54db7347 |
| name\[]          |                                      |
| tag\_id\[]       |                                      |
| status\_id       |                                      |
| limit            |                                      |
| page             |                                      |

### **Example Response**

{% code lineNumbers="true" %}
```json
 "data": {
        "type": "success",
        "title": "Load successfully",
        "content": [
            {
                "uuid": "992bd6f1-0a4c-40b2-88c0-d6ae54db7347",
                "directory": "2023/05/15",
                "file_name": "e332938226517443e5ca72b5d269a0a6.zip",
                "can_be_running": true,
                "proxy": "",
                "created_at": "2023-05-15T07:28:07.000000Z",
                "created_at_diff": "43 minutes ago",
                "id": 20165,
                "folder_id": 532,
                "check_open": 1,
                "name": "15 - 5",
                "version": 112,
                "browser_type": "hidemium",
                "os": "mac",
                "note": "",
                "last_open": "2023-05-15 14:30:53",
                "last_open_diff": "41 minutes ago",
                "transfer": "",
                "source_version": null,
                "shares_role": false,
                "shared_uuid": "",
                "status": null,
                "status_chil": 0,
                "tags": [],
                "status_id": null,
                "listing": null
            }
        ]
    },
    "links": {
        "first": "https://v2-api.multibrowser.io/v1/browser/list?page=1",
        "last": "https://v2-api.multibrowser.io/v1/browser/list?page=1",
        "prev": null,
        "next": null
    },
    "meta": {
        "current_page": 1,
        "from": 1,
        "last_page": 1,
        "path": "https://v2-api.multibrowser.io/v1/browser/list?page=1",
        "per_page": "10",
        "to": 1,
        "total": 1
    }
}
```
{% endcode %}
