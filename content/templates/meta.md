---
title: meta
---
<%* if (tp.file.title.includes("TDS ")) { %>
<%tp.file.include("[templates/The Daily Stoic Template](None)")%>
<%* } else if ( tp.file.title.charAt(0).toUpperCase() != tp.file.title.charAt(0).toLowerCase() ) { %>
<%tp.file.include("[templates/Note Template](None)")%>
<%* } else if (tp.file.title.charAt(0) == "{" && tp.file.title.includes("Application")) { %>
<%tp.file.include("[templates/Book Application Template](None)")%>
<%* } else if (tp.file.title.substring(0, 2) == "!M") { %>
<%tp.file.include("[templates/Meal Idea Template](None)")%>
<%* } else if (tp.file.title.charAt(0) == "{") { %>
<%tp.file.include("[templates/Inputs/Book Notes Template](None)")%>
<%* } else if (tp.file.title.includes("2021-W")) { %>
<%tp.file.include("[templates/Weekly Review Template](None)")%>
<%* } else if (tp.file.title.includes("TDS ")) { %>
<%tp.file.include("[templates/The Daily Stoic Template](None)")%>
<%* } else if (tp.file.title.charAt(0) == "@") { %>
<%tp.file.include("[templates/People Template](None)")%>
<%* } else if (tp.file.title.includes("MOC")) { %>
<%tp.file.include("[templates/MOC Template](None)")%>
<%* } else if (tp.file.title.includes("---")) { %>
<%tp.file.include("[templates/Quote Template](None)")%>
<%* } else if (tp.file.title.substring(0, 2) == "!V") { %>
<%tp.file.include("[templates/Video Idea Template](None)")%>
<%* } else if (tp.file.title.charAt(0) == "%") { %>
<%tp.file.include("[templates/Inputs/Podcast](None)")%>
<%* } else if (tp.file.title.charAt(0) == "'") { %>
<%tp.file.include("[templates/Inputs/Classes Template](None)")%>
<%* } else if (tp.file.title.charAt(0) == "+") { %>
<%tp.file.include("[templates/Inputs/Youtube](None)")%>
<%* } else if (tp.file.title.charAt(0) == "(") { %>
<%tp.file.include("[templates/Inputs/Article](None)")%>
<%* } else if (tp.file.title.charAt(0) == ")") { %>
<%tp.file.include("[templates/Inputs/Course Template](None)")%>
<%* } else if (tp.file.title.charAt(0) == "&") { %>
<%tp.file.include("[templates/Inputs/Paper](None)")%>
<%* } else if (tp.file.title.charAt(0) == "=") { %>
<%tp.file.include("[templates/Inputs/Thought](None)")%>
<%* } else if (tp.file.title.charAt(0) == "~") { %>
<%tp.file.include("[templates/Project Template](None)")%>
<%* } else { %>
<%tp.file.include("[templates/Note Template](None)")%>
<%* } %>