[[Home]]

#map  

# {{Value}}
```dataview
list
where contains(file.folder, this.file.folder) and !contains(file.name, this.file.name)
```