---
layout: post
title:  "Check What Processes Are Running"
description: "Command to check what processes are running on the computer."
date:   2016-04-30 22:15:00 +0530
categories: shell
---

Command to list all the running processes.

```sh
$ ps -ef
```

Command to list all running processes by a specific user.

```sh
$ pgrep -l -u <username>
```
The above command can also be written as:

```sh
$ ps -ef | grep <username>
```