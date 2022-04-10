<%* if (tp.file.title.includes("TDS ")) { %>
<%tp.file.include("[[templates/The Daily Stoic Template]]")%>
<%* } else if ( tp.file.title.charAt(0).toUpperCase() != tp.file.title.charAt(0).toLowerCase() ) { %>
<%tp.file.include("[[templates/Note Template]]")%>
<%* } else if (tp.file.title.charAt(0) == "{" && tp.file.title.includes("Application")) { %>
<%tp.file.include("[[templates/Book Application Template]]")%>
<%* } else if (tp.file.title.substring(0, 2) == "!M") { %>
<%tp.file.include("[[templates/Meal Idea Template]]")%>
<%* } else if (tp.file.title.charAt(0) == "{") { %>
<%tp.file.include("[[templates/Inputs/Book Notes Template]]")%>
<%* } else if (tp.file.title.includes("2021-W")) { %>
<%tp.file.include("[[templates/Weekly Review Template]]")%>
<%* } else if (tp.file.title.includes("TDS ")) { %>
<%tp.file.include("[[templates/The Daily Stoic Template]]")%>
<%* } else if (tp.file.title.charAt(0) == "@") { %>
<%tp.file.include("[[templates/People Template]]")%>
<%* } else if (tp.file.title.includes("MOC")) { %>
<%tp.file.include("[[templates/MOC Template]]")%>
<%* } else if (tp.file.title.includes("---")) { %>
<%tp.file.include("[[templates/Quote Template]]")%>
<%* } else if (tp.file.title.substring(0, 2) == "!V") { %>
<%tp.file.include("[[templates/Video Idea Template]]")%>
<%* } else if (tp.file.title.charAt(0) == "%") { %>
<%tp.file.include("[[templates/Inputs/Podcast]]")%>
<%* } else if (tp.file.title.charAt(0) == "'") { %>
<%tp.file.include("[[templates/Inputs/Classes Template]]")%>
<%* } else if (tp.file.title.charAt(0) == "+") { %>
<%tp.file.include("[[templates/Inputs/Youtube]]")%>
<%* } else if (tp.file.title.charAt(0) == "(") { %>
<%tp.file.include("[[templates/Inputs/Article]]")%>
<%* } else if (tp.file.title.charAt(0) == ")") { %>
<%tp.file.include("[[templates/Inputs/Course Template]]")%>
<%* } else if (tp.file.title.charAt(0) == "&") { %>
<%tp.file.include("[[templates/Inputs/Paper]]")%>
<%* } else if (tp.file.title.charAt(0) == "=") { %>
<%tp.file.include("[[templates/Inputs/Thought]]")%>
<%* } else if (tp.file.title.charAt(0) == "~") { %>
<%tp.file.include("[[templates/Project Template]]")%>
<%* } else { %>
<%tp.file.include("[[templates/Note Template]]")%>
<%* } %>