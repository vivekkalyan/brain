# {{title}}

## Goals

- [ ] 
## Events

- 
## Log


## Today's Created Notes

```dataview
LIST WITHOUT ID "[[" + file.path + "|" + file.aliases[0] + "]]"
WHERE striptime(date(file.name, "X")) = date(this.file.aliases[0])
SORT file.name
```