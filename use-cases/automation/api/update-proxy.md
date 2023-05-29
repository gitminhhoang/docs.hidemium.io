---
description: Update proxy
---

# UPDATE PROXY

### **Request**

<table><thead><tr><th width="249">Method</th><th>URL</th></tr></thead><tbody><tr><td>PUT</td><td><a href="http://127.0.0.1:5555/update-proxy">http://127.0.0.1:5555/update-proxy</a></td></tr></tbody></table>

#### **Body**

{% code lineNumbers="true" %}
```json
{
    "uuid": "992d5efd-7709-4f2b-a1b1-50a16ca2b3bf",
    "title": "title",
    "ip": "222.22.22.222",
    "port": "222",
    "user": "222",
    "pass": "222",
    "type": "HTTP",
    "note": "note",
    "details": {
        "ip": "141.95.19.6s5",
        "hostname": "vps-efd874c9.vps.ovh.net",
        "city": "Limburg an der Lahn",
        "region": "Hesse",
        "country": "CA",    
        "loc": "50.3836,8.0503",
        "org": "AS16276 OVH SAS",
        "postal": "65549",
        "timezone": "Europe/Berlin",
        "asn": {
            "asn": "AS16276",
            "name": "OVH SAS",
            "domain": "ovh.net",
            "route": "141.95.0.0/17",
            "type": "hosting"
        }
    }
}
```
{% endcode %}

* uuid: UUID of proxy, need to use API _**list profile**_ to get proxy's UUID
* ip: IP address
* port: access port
* user: username of proxy
* pass: Password of proxy
* type: proxy type (HTTP, SOCKS4, SOCKS5, SSH)
* details: detailed information of proxy: ip, location, org, city, region, country, timezone, asn.

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
