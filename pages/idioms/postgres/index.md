---
layout: page
title: Postgres
---

# Creating user/role
`sudo -u postgres createuser $USER
sudo -u postgres psql -c "alter user $USER with superuser" postgres`
