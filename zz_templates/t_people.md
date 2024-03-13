---
location:
ancestry:
---
<%*
	let title = tp.file.title 
	if (title.startsWith("Untitled")) {
		title = await tp.system.prompt("Title");
		await tp.file.rename(`${title}`);
	}
%>
# <%* tR += `${title}` %>

## Interactions
<% tp.file.cursor() %>

### Related Characters

## Picture
