## Project 7 - WordPress Pentesting

Time spent: **15** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. Unauthenticated Stored Cross-Site Scripting (XSS)
  - [X] Summary: Current versions of WordPress are vulnerable to a stored XSS. An unauthenticated attacker can inject JavaScript in WordPress comments. The script is triggered when the comment is viewed. If triggered by a logged-in administrator, under default settings the attacker can leverage the vulnerability to execute arbitrary code on the server via the plugin and theme editors. Alternatively the attacker could change the administrator’s password, create new administrator accounts, or do whatever else the currently logged-in administrator can do on the target system.  
    - Vulnerability types: XSS
    - Tested in version: 4.2, 4.1.2, 4.1.1, 3.9.3 
    - Fixed in version: 4.2.1
  - [X] GIF Walkthrough: ![xss vulnerability1](https://user-images.githubusercontent.com/36680097/40211520-fece42de-59ff-11e8-82b6-983d41808b16.gif)

  - [X] Steps to recreate: Reading the above vulnerabilty, this is how I went about it,
        1) I looked up the vulnerabilty in this website https://klikki.fi/adv/wordpress2.html
        2) I copied the code that shows the vulnerabilty for the XSS attack. 
            ***<a title='x onmouseover=alert(unescape(/hello%20world/.source)) style=position:absolute;left:0;top:0;width:5000px;                height:5000px  AAAAAAAAAAAA...[64 kb]..AAA'></a>***
        3) I as a user injected the above code into the the comments section. In this scenerio I was the attacker. Injecting the code      
           above exploited the vulnerability. It displays a "Hello World" box whenever a user loads a page.
  - [X] Affected source code:
     <textarea id="comment" name="comment" cols="45" rows="8" aria-describedby="form-allowed-tags" aria-required="true"      required="required" data-gramm="true" data-txt_gramm_id="bd582786-fe34-3cf3-2756-b92e2409e51c" data-gramm_id="bd582786-fe34-3cf3-2756-b92e2409e51c" spellcheck="false" data-gramm_editor="true" style="background: transparent none repeat scroll 0% 0% !important; z-index: auto; position: relative; line-height: 24px; font-size: 16px; transition: none 0s ease 0s;"></textarea>
     
2. FingePrinting Exposed Readme
  - [X] Summary: A file exist exposing a version number.
    - Vulnerability types: This can be found in various versions of Wordpress
    - Tested in version: 4.2
    - Fixed in version: Can be fixed in any version. readme.html must be deleted whenever a user updates wordpress.
  - [X] GIF Walkthrough: ![fingerprint](https://user-images.githubusercontent.com/36680097/40211596-5ade3e6c-5a00-11e8-8e1d-c279eb3f715e.gif)

  - [X] Steps to recreate: 1)visit wpdistillery.vm
                           2)In the url add /readme.html
  - [X] Affected source code:vmdistillery.vm/readme.html
    
3. Application Denial of Service (DOS) (unpatched)
  - [X] Summary: This is a vulnerability that affects almost all versions of word press and is used by running a Python Script. The python script loads a lot of javascript that ends up overloading the website
    - Vulnerability types: DOS
    - Tested in version: 4.94 and below
    - Fixed in version: 4.95
  - [X] GIF Walkthrough: ![dos](https://user-images.githubusercontent.com/36680097/40211676-c83193c4-5a00-11e8-933d-db24a03fa894.gif)


  - [X] Steps to recreate: 1) Make sure all vm's are up and running along with wpdistillery.vm
                           2) Make open kali linux terminal and run doser.py script
                           3) Look at wpdistiller.vm and attemp to refresh. The website cannot reload and will crash
  - [X] Affected source code: http://wpdistillery.vm
  

## Assets
WP-Scan
dosser.py
Google

## Resources
Whttps://wpsmackdown.com/delete-unnecessary-wordpress-files/ordpress directory

Unathenticated Stored Cross-Site Scripting (XSS)
    Reference: https://wpvulndb.com/vulnerabilities/7945
    Reference: http://klikki.fi/adv/wordpress2.html
    Reference: http://packetstormsecurity.com/files/131644/
    Reference: https://www.exploit-db.com/exploits/36844/
   
Application Denial of Service (DoS) (unpatched)
    Reference: https://wpvulndb.com/vulnerabilities/9021
    Reference: https://baraktawily.blogspot.fr/2018/02/how-to-dos-29-of-world-wide-websites.html
    Reference: https://github.com/quitten/doser.py
    Reference: https://thehackernews.com/2018/02/wordpress-dos-exploit.html
    Reference: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-6389

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Many of the challenges that I encountered involved the virtual machines not functioning properly. Also vmdistillery.vm often would no longer work and I had to uninstall and reinstall many times. Alot of these exploits took a long time, however, this was a good thing because it allowed me to step to into the mind of a hacker. I understood these vulnerabilites a lot more after this challenge.

## License

    Copyright [2018] [Manuel Vazquez]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
