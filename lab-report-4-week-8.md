# Week 8 Lab Report 4

## Links to MarkdownParse Repositories
-[my repo](https://github.com/YLuo0216/markdown-parse-Yvonne)
-[review group repo](https://github.com/samw0627/markdownparse2/blob/main/MarkdownParse.java)

## Snippet 1
- should produce: ``[`google.com]``
- code for MarkdownParseTest.java  
```
@Test
    public void labReportSnippet1() throws IOException {
        Path filename = Path.of("lab-report-snippet1.md");
        String contents = Files.readString(filename);
        assertEquals(List.of("`google.com"), MarkdownParse.getLinks(contents));
    }
```

## Snippet 2
- should produce: `[a.com(()), example.com]`
- code for MarkdownParseTest.java  
```
@Test
    public void labReportSnippet2() throws IOException {
        Path filename = Path.of("lab-report-snippet2.md");
        String contents = Files.readString(filename);
        assertEquals(List.of("a.com(())", "example.com"), MarkdownParse.getLinks(contents));
    }
```

## Snippet 3
- should produce: `[https://ucsd-cse15l-w22.github.io/]`
- code for MarkdownParseTest.java  
```
@Test
    public void labReportSnippet3() throws IOException {
        Path filename = Path.of("lab-report-snippet3.md");
        String contents = Files.readString(filename);
        assertEquals(List.of("https://ucsd-cse15l-w22.github.io/"), MarkdownParse.getLinks(contents));
    }
```
