---
description: >-
  https://documenter.getpostman.com/view/17474604/2sA3JM61j5#a346b7bd-c715-48b9-8837-9ea60a40d3f9
---

# Update campaign input variable

### **Example Request** <a href="#example-request-1" id="example-request-1"></a>

<table><thead><tr><th width="145">Method</th><th>URL</th></tr></thead><tbody><tr><td>POST</td><td><a href="http://localhost:2222/automation/campaign/save-auto-campaign">http://localhost:2222/automation/campaign/save-auto-campaign</a></td></tr></tbody></table>

### Body <a href="#params" id="params"></a>

```
{
    "campaignId": "26", //Use the Get campaign API to get the ID
    "input": [
        {
            "id": "80cefb86-e28c-4528-a07c-d04f7423ee70",
            "value": "row_index",
            "label": "row_index",
            "data": "",
            "name": ""
        },
        {
            "id": "9937a16d-c090-4370-a95b-9a6d233f9598",
            "value": "email",
            "label": "email",
            "data": "",
            "name": ""
        },
        {
            "id": "c5aa3aba-d3fd-4294-99ca-f2a5f0cd84e8",
            "value": "password",
            "label": "password",
            "data": "",
            "name": ""
        },
        {
            "id": "d6ec5deb-3377-4f51-9f01-145a7cdfb6a2",
            "label": "file_xlsx_path",
            "value": "file_xlsx_path",
            "data": "D:\\helo.xlsx"
        }
    ]
}
```

The INPUT part in the body you can get from the Get campaign API.

<figure><img src="../../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### **Example Response** <a href="#id-3.-example-response" id="id-3.-example-response"></a>

```

{
   //content
}
```
