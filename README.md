
# Custom-Action-

A custom action, which prints "This is the entrypoint script."

## Events
Push event is used to trigger the workflow

## Code

Dockerfile code which uses ubuntu as the base image, and uses entrypoint.sh executable that will execute when the container is launched.
```Dockerfile
FROM ubuntu

COPY entrypoint.sh /entrypoint.sh
RUN chmod +x /entrypoint.sh

ENTRYPOINT ["/entrypoint.sh"]
```

entrypoint.sh code: 
This code is executed when container is launched.

```
#!/bin/bash

echo "This is the entrypoint script."
```
