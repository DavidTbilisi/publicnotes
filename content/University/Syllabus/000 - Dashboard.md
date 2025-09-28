
## Filtered By Semester
```dataview
table semester, title, status
from "content/University/Syllabus" where semester = 7
and contains(status, "todo")

```


## Done
```dataview
table semester
from "content/University/Syllabus"
where contains(status, "done")
sort semester
```

## Doing
```dataview
table semester
from "content/University/Syllabus"
where contains(status, "doing")
sort semester
```


## Todo ( Mandatory )
```dataview
table title, semester
from "content/University/Syllabus" where required = true 
and !contains(status, "done") and !contains(status, "doing")
sort semester asc
```


## Todo (!Mandatory)
```dataview
table title, want
from "content/University/Syllabus" where required = false 
and !contains(status, "done") and !contains(status, "doing") and want > 0
sort want desc
```
