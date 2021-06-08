# Markdown to Asciidoc cheatsheet

| Element | Markdown | Asciidoc |
| ------- | -------- | -------- |
| Headings:<br>- h1 <br>- h2<br>- h3 | <br> `# Title` <br> `## Title` <br> `### Title` | <br> `= Title` <br> `== Title` <br> `=== Title` |
| **Bold** | `**text**` | `*bold*` |
| _Italic_ | `_text_` | `_text_` |
| Horizontal Rule | `---` | <code>&#96;&#96;&#96;</code> |
| Quote | `> text` | <pre>[quote, cite author, cite source]<br>\_\_\_\_<br>text<br>\_\_\_\_</pre> |
| `Code` | <code>\`text\`</code> | <code>\`text\`</code> |
| Code Block | <pre>\`\`\`lang<br>code here<br>\`\`\`</pre> | <pre>[source,lang]<br>----<br>code here<br>----</pre> |
| Link URL | `[text](url)` | `url[text]` |
| Link Relative | `[text](/path)` | `link:/path[text]` |
| Tables | <pre>\| Header 1 \| Header 1 \|<br>\| -------- \| -------- \|<br>\| col one  \| col two  \| </pre> | <pre>[options="header"]<br>\|=======================<br>\|Header 1  \|Header 2<br>\|col one   \|col two<br>\|=======================</pre> |
| Ordered List | <pre>1. one<br>1. two<br>1. three</pre> | <pre>. one<br>. two<br>. three</pre> |
| Unordered List | <pre>- one<br>- two<br>- three</pre> | <pre>* one<br>* two<br>* three</pre> |
| Task/Check List | <pre>- [ ] task a<br>- [x] task b<br>- [ ] task c</pre> | <pre>* [ ] task a<br>* [x] task b<br>* [ ] task c</pre> |
| Images:<br>- Inline <br>- Block | <br>`![alt text](url)`<br>`![alt text](url)` *<br> * <sub>(new line above and below)</sub> | <br>`image:url[alt text]`<br>`image::url[alt text]` |

---

Asciidoc Code Blocks with Callouts
```adoc
====
[source,lang]
----
line of code // <.>
line of code # <.>
line of code ;; <.>
line of code <!--.-->
----
<.> multiple types of comments are supported
<.> Bash Ruby, Python, Perl, etc.
<.> even double semicolon
<.> and XML
====
```

