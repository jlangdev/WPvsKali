# Project 7 - WordPress Pentesting

Time spent: **8** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1.  Unauthenticated Stored Cross-Site Scripting CVE-2015-3440
  - [ ] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.1
    - Fixed in version: 4.2.1
  - [ ] GIF Walkthrough: 
  
  ![AAA](https://github.com/jlangdev/WPvsKali/blob/master/64AAA.gif)
  - [ ] Steps to recreate: 
      - Use some sort of program or text generator to generate 64KB worht of text
      - Submit the following as a comment
      ```
      <a title='x onmouseover=alert(unescape(/hello%20world/.source)) style=position:absolute;left:0;top:0;width:5000px;height:5000px  [INSERT YOUR 64KB OF TEXT HERE WITHOUT THESE SQUARE BRACKETS]'></a>
      ```
      - Once approved, the script will execute when the comment is loaded
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
2. Publish Post & Mark as Sticky Permission Issue ID WPVDB-ID:8188
  - [ ] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.1
    - Fixed in version: 4.1.8
  - [ ] GIF Walkthrough: 
  
    ![Sticky](https://github.com/jlangdev/WPvsKali/blob/master/sticky.gif)
  - [ ] Steps to recreate: 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
3. Authenticated Stored Cross-Site Scripting wordpress DCVE-2015-5622
  - [ ] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.1
    - Fixed in version: 4.2.2
  - [ ] GIF Walkthrough: 
  
     ![Contributor](https://github.com/jlangdev/WPvsKali/blob/master/Contributor.gif)
  - [ ] Steps to recreate: 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
 
