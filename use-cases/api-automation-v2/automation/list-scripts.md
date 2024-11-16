---
description: Returns a list of scripts (workflows)
---

# List scripts

### Request

| Method | URL                             |
| ------ | ------------------------------- |
| GET    | http://scripts?page=1\&limit=10 |

| Params | Value | Description                  |
| ------ | ----- | ---------------------------- |
| page   | 1     | page number of pagination    |
| limit  | 10    | number of profiles displayed |

### Example request (Hidemium V2)

| Method | URL                                                                                              |
| ------ | ------------------------------------------------------------------------------------------------ |
| GET    | [http://127.0.0.1:5555/scripts?page=1\&limit=10](http://127.0.0.1:5555/scripts?page=1\&limit=10) |

### Example request (Hidemium V4)

<table><thead><tr><th width="184">Method</th><th>URL</th></tr></thead><tbody><tr><td>GET</td><td><a href="http://127.0.0.1:2222/v2/automation/script?page=1&#x26;limit=10">http://127.0.0.1:2222/v2/automation/script?page=1&#x26;limit=10</a></td></tr></tbody></table>

### **Response**

```json
 "data": {
        "type": "success",
        "title": "Request successfully.",
        "content": [
                //content information 
                ]
        }
```
