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
