---
layout: page
title: VSCode idioms
---


## Compile and refresh pdf on save example using lilypond

### tasks.json
```
{
  "version": "2.0.0",
  "tasks": [
    {
      "label": "Compile",
      "command": "lilypond sand.ly",
      "type": "shell",
      "args": [],
    },
    {
      "label": "Refresh pdf", 
      "dependsOn": "Compile", 
      "command": "${command:latex-workshop.refresh-viewer}" 
    }
  ],
}
```

### settings.json
```
{
  "triggerTaskOnSave.tasks": {
    "Refresh pdf": [
      "**/*.ly"
    ],
  },
}
```