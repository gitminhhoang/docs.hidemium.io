---
description: Update proxy of profile
---

# UPDATE PROXY PROFILE

### **Request**

| Method | URL                                                                                      |
| ------ | ---------------------------------------------------------------------------------------- |
| POST   | [http://127.0.0.1:5555/update-proxy-profile](http://127.0.0.1:5555/update-proxy-profile) |

#### **Body**

{% code lineNumbers="true" %}
```json
{
    "browser_update":[
        {
            "uuid":"99321674-b6c5-4004-a182-be6147beea3e",
            "proxy":"SOCKS5|192.168.30.51|8080|123|121"
        }
    ]
}
```
{% endcode %}

* uuid: UUID of profile
* proxy: Proxy wants to update to profile, in the format: **type|ip\_address|port|username|pass**

### **Response**

{% code lineNumbers="true" %}
```json
{
    "type": "success",
    "title": "Edit successfully.",
    "content": []
}
```
{% endcode %}
