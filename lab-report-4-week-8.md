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
- For my repo:  Junit test failed. Output: ![mine1](mine1.png)
- For review group: Junit test failed. Output: ![review1](review1.png)

## Snippet 2
- should produce: `[a.com, a.com(()), example.com]`
- code for MarkdownParseTest.java  
```
@Test
    public void labReportSnippet2() throws IOException {
        Path filename = Path.of("lab-report-snippet2.md");
        String contents = Files.readString(filename);
        assertEquals(List.of("a.com(())", "example.com"), MarkdownParse.getLinks(contents));
    }
```  
- For my repo:  Junit test failed. Output: ![mine3](mine2.png)
- For review group: Junit test failed. Output: ![review3](review2.png)

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
- For my repo:  Junit test failed. Output: ![mine3](mine3.png)
- For review group: Junit test failed. An infinite loop appeared, so there actually isn't any output. Output: ![review3](review3.png)

## Answer the following questions with 2-3 sentences each:
- Do you think there is a small (<10 lines) code change that will make your program work for snippet 1 and all related cases that use inline code with backticks? If yes, describe the code change. If not, describe why it would be a more involved change.
- Do you think there is a small (<10 lines) code change that will make your program work for snippet 2 and all related cases that nest parentheses, brackets, and escaped brackets? If yes, describe the code change. If not, describe why it would be a more involved change.
- Do you think there is a small (<10 lines) code change that will make your program work for snippet 3 and all related cases that have newlines in brackets and parentheses? If yes, describe the code change. If not, describe why it would be a more involved change.
