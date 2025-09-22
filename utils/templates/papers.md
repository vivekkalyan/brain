<%*
let title = tp.file.title
if (title.startsWith("Untitled")) {
	try {
		title = await tp.system.prompt("Title", null, true, false);
	} catch {
		const file = tp.file.find_tfile(tp.file.path(true));
		await app.vault.delete(file);
	}
}
const url = await tp.system.prompt("URL");

app.fileManager.processFrontMatter(tp.file.find_tfile(tp.file.path(true)), (frontmatter) => {
  frontmatter["url"] = url;
});
-%>
<% await tp.file.rename(tp.file.creation_date("X")) -%>
---
author: []
url: <%* if (url) { %>"<%= url %>"<%* } %>
topics: []
video:
tags:
- paper
- to-read
---

<% "# " + title %>

# Notes

# Thoughts
