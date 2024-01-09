<%*
let title = tp.file.title
if (title.startsWith("Untitled")) {
	title = await tp.system.prompt("Title");
}
-%>
<% await tp.file.rename(tp.file.creation_date("X")) -%>
---
title: <% title %>
author:
rating:
start_read:
end_read:
tags:
---

<% "# " + title %>
