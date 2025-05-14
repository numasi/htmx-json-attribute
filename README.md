### HTMX extension for sending plain JSON data defined at attribute level (w/o HTML form) 

## Use

Clone repo, grab and link json-attribute.js

```
<meta name='htmx-config' content='{"selfRequestsOnly":false}'>
<script src='https://unpkg.com/htmx.org@2.0.4'></script>
<script src='json-attribute.js'></script>
<div
  hx-post='https://api.hive.blog'
  hx-trigger='load'
  hx-swap='outerHTML'
  hx-target='div'
  hx-ext='json-attr'
  hx-json='{
    "jsonrpc": "2.0",
    "method": "condenser_api.get_blog_entries",
    "params": ["numasi", 0, 10],
    "id": 1
  }'
></div>
```
See full example at [this repo](https://github.com/numasi/htmx-examples)