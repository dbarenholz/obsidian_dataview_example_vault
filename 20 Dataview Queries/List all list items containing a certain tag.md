---
description: List all bullet points that contain a certain tag
topics:
  - filter bullet points
---
#dataviewquery
#dv/list #dv/from #dv/where #dv/flatten #dv/contains

# List all list items containing a certain tag

## Basic 

```dataview
LIST WITHOUT ID L.text
FROM "10 Example Data/dailys"
FLATTEN file.lists AS L
WHERE contains(L.tags, "#tag1")
```

> [!help]- Similar Queries
> Maybe these queries are of interest for you, too:
> ```dataview
> LIST
> FROM "20 Dataview Queries"
> FLATTEN topics as flattenedTopics
> WHERE contains(this.topics, flattenedTopics)
> AND file.name != this.file.name
> ```