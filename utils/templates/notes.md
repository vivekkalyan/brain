<%*
let title = tp.file.title
if (title.startsWith("Untitled")) {
	title = await tp.system.prompt("Title");
}
if (title === null) {
	title = ""
}
-%>
<% await tp.file.rename(tp.file.creation_date("X")) -%>
---
tags:
---

<% "# " + title %>
