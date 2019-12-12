# `values`

Like `list` but only shows unique values.

Ex: Unique websites visited by each user.

```
index=network sourcetype=cisco_wsa_squid
| stats values(s_hostname) by cs_username
```
