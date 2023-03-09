tags:: #map/view 

# Spaces
```dataview
list
from "Spaces" and #map/view 
sort file.name desc
```

# New Notes
These notes need to be sorted.
``` dataview
TABLE WITHOUT ID
 file.link as "New Notes",
 (date(today) - file.cday).day as "Days Alive"

FROM "+ Notes" and -#on/readme 

SORT file.cday asc

LIMIT 50
```

# Recent Meetings
Latest notes from Meetings folder
``` dataview
TABLE WITHOUT ID
 file.cday as "Day",
 file.link as "Meeting"
 
FROM "Calendar" and #log/meeting 

SORT file.cday asc

LIMIT 20
```

# Daily Notes
Latest notes from Calendar folder.
``` dataview
TABLE WITHOUT ID
 file.cday as "Day",
 file.link as "Daily Note"
 
FROM "Calendar" and #log/journal  

SORT file.cday asc

LIMIT 10
```
