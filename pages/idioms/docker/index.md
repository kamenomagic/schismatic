---
layout: page
title: Docker
---

## Docker compose error:
After executing something like `docker-compose up`

```
Traceback (most recent call last):
  File "docker-compose", line 6, in <module>
  File "compose/cli/main.py", line 71, in main
  File "compose/cli/main.py", line 127, in perform_command
  File "compose/cli/main.py", line 1085, in up
  File "compose/cli/main.py", line 1081, in up
  File "compose/project.py", line 527, in up
  File "compose/service.py", line 348, in ensure_image_exists
  File "compose/service.py", line 368, in image
  File "site-packages/docker/utils/decorators.py", line 17, in wrapped
docker.errors.NullResource: Resource ID was not provided
```
