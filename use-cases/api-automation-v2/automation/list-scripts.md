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

### Example request&#x20;

| Method | URL                                                                                              |
| ------ | ------------------------------------------------------------------------------------------------ |
| GET    | [http://127.0.0.1:5555/scripts?page=1\&limit=10](http://127.0.0.1:5555/scripts?page=1\&limit=10) |

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
