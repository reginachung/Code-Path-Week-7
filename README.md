# Project 7 - WordPress Pentesting

Time spent: **10** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. (Required) Unauthenticated Stored Cross-Site Scripting (XSS)
  - [ ] Summary: Large text file in the comment will cause the website to break.
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.1
  - [ ] GIF Walkthrough: ![](https://user-images.githubusercontent.com/35437875/38159256-bdcef75e-3472-11e8-9e63-be944937a01b.gif)
  - [ ] Steps to recreate:  Go to website linked under "affected source code" and copy the code noted under "Proof of Concept". Go to the wordpress website (not as admin), view a post and fill in the reply's comment with the copied text. When inputting in the text, substitute "AAAAA .. [64kb]//AAA" with a 64kb text file. Post the reply and note the alert that pops up with the broken website.
  - [ ] Affected source code:
    - [Link 1](https://klikki.fi/adv/wordpress2.html)
1. (Required) Authenticated Stored Cross-Site Scripting (XSS)
  - [ ] Summary: When hovering over the post's link, an alert popped up.
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.3
  - [ ] GIF Walkthrough: ![](https://user-images.githubusercontent.com/35437875/38166238-6eac7b2a-34ee-11e8-8f6d-b8e88cc15f97.gif)
  - [ ] Steps to recreate: Go to the link noted under "affected source code" and copy the first code noted under "details". Make a new post as admin and input the copied text into the body of the post. Then submit and view the post to see an alert come up when hovering over the post's link. 
  - [ ] Affected source code:
    - [Link 1](https://klikki.fi/adv/wordpress3.html)
1. (Required) Authenticated Stored Cross-Site Scripting (XSS) in YouTube URL Embeds
  - [ ] Summary: When embeding a Youtube URL in the post with a script alert, an alert will come up.
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.13
  - [ ] GIF Walkthrough: ![](https://user-images.githubusercontent.com/35437875/38166571-ea1cf19a-34f3-11e8-9919-4c01a11de7c1.gif)
  - [ ] Steps to recreate: When making a new post, input in the body: https://www.youtube.com/watch?v=<SCRIPT>alert('XSS')</SCRIPT> 
Then highlight the url to insert a link, this will cause an alert to popup. 
  - [ ] Affected source code:
    - [Link 1](https://github.com/WordPress/WordPress/commit/419c8d97ce8df7d5004ee0b566bc5e095f0a6ca8)
1. (Optional) Vulnerability Name or ID
  - [ ] Summary: 
    - Vulnerability types:
    - Tested in version:
    - Fixed in version: 
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
1. (Optional) Vulnerability Name or ID
  - [ ] Summary: 
    - Vulnerability types:
    - Tested in version:
    - Fixed in version: 
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php) 

## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Describe any challenges encountered while doing the work

## License

    Copyright [yyyy] [name of copyright owner]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
