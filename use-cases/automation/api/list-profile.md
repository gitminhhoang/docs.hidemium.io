---
description: Returns a list of profiles
---

# LIST PROFILE

### Request

| Method | URL                                  |
| ------ | ------------------------------------ |
| GET    | api\_url/profileList?page=1\&limit=1 |

| Params           | Values   | Description                                            |
| ---------------- | -------- | ------------------------------------------------------ |
| page             | number   | page number of pagination                              |
| limit            | number   | number of profiles displayed                           |
| browser\_uuid\[] | string   | profile uuid                                           |
| name\[]          | string   | the name of the profile                                |
| folder\_id\[]    | number   | folder id                                              |
| tag\_id\[]       | number   | tag id                                                 |
| status\_id       | number   | status id of profile                                   |
| date\_range\[]   | datetime | profile creation date (from date) (format: yyyy-mm-dd) |
| date\_range\[]   | datetime | profile creation date (to date) (format: yyyy-mm-dd)   |

### **Example Request**

| Status | Response                                                                                                 |
| ------ | -------------------------------------------------------------------------------------------------------- |
| GET    | [http://127.0.0.1:5555/profileList?page=1\&limit=10](http://127.0.0.1:5555/profileList?page=1\&limit=10) |

**Params**

| Key              | Value                                |
| ---------------- | ------------------------------------ |
| page             | 1                                    |
| limit            | 10                                   |
| browser\_uuid\[] | 98a75178-4d0f-4e9f-8aa9-ae832549aac3 |
| name\[]          |                                      |
| folder\_id\[]    |                                      |
| tag\_id\[]       |                                      |
| status\_id       |                                      |
| date\_range\[]   |                                      |
| date\_range\[]   |                                      |

### **Example Response**

{% code lineNumbers="true" %}
```json
"data": {
        "type": "success",
        "title": "Load successfully",
        "content": [
            {
               //content information
            }
        ]
    },
    "links": {
        "first": "https://dev-api.minhhoangjsc.io/v1/browser/list?page=1",
        "last": "https://dev-api.minhhoangjsc.io/v1/browser/list?page=1",
        "prev": null,
        "next": null
    },
    "meta": {
        "current_page": 1,
        "from": 1,
        "last_page": 1,
        "path": "https://dev-api.minhhoangjsc.io/v1/browser/list",
        "per_page": "10",
        "to": 1,
        "total": 1
    }
}
```
{% endcode %}
