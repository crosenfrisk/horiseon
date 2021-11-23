# Horiseon Refactor Project

## Table of Contents

* [Description](#Description)
* [What I Did](#What-I-Did) 
* [My Approach](#My-Approach) 
* [Implementation](#Implementation)

* [Lessons Learned](#Lessons-Learned) 
* [Problems Solved](#Problems-Solved) 
* [Code Improvement and Performance](#Code-Improvement-and-Performance) 

* [Installation](#Installation) 
* [Usage](#Usage)
* [Credits](#Credits)

* [Articles from the Internet](#Articles-from-the-Internet) 
* [Accessibility Tools](#Accessibility-Tools)

* [License](#License)

### Description

This repository (Refactor Horiseon) was created for a bootcamp challenge project. The original source code came from: coding-boot-camp/urban-octo-telegram . 

Our "client" Horiseon is a fictional marketing agency who has requested to have their code adjusted to meet accessiblility standards for websites and optimized for search engine performance.


## WHAT I DID

To help with accessibility, I first looked at the `index.html file`, which I quickly noticed had a lot of redundant text. Inside the body it seemed like everything was a `<div>`. *Note: The original/source code can be referenced in a docuement I renamed `SOURCE-index.html`.*

I cleaned up the `<head>` and added a proper `<title>` which tells the user of the website where they are, with "Home - Horiseon" visable in the browser tab.


Within newly named `<header>` section, I noticed a `<span>` element within the `<h1>` element, which I removed ( `.seo {}` was also removed from the CSS) for cleaner copy. I have yet to discuss with the client what their intent was, but my concern was that any screen readers trying to introduce the `<h1>` element to their reader/user may get caught up within the styling of the word. However, if the client prefers I can revert it to the previous style using the `<span>` element to seperate out SEO from HoriSEOn. 

*Edit, I returned the .seo {} to style.css, and returned the `<span>` element within `<h1>` of the `<header>` to match the mockup. This decision was made after talking with a cohort member (Megan M.). She made a good point about matching the brief. After testing readability using the Narrator application on my PC I felt good knowing the user would hear the proper `<h1>` introduction without any gibberish in between. Now I have a better understanding on how the `<span>` element works.*
  
To help with readability of the `index.html` file, I added `<!-- -->` comments to delineate sections and their purpose within the document.

I added `<nav>` elements which seemed a better description for screen readers and backend web users than simply `<div>` within the `<header>` section.
  
`<header>` elements were renamed within the CSS document. Since there were no class attributes for `<header>`, we did not need `.header {}`. Subsequent `.header {}` styles were renamed to `header {}.` Additionally, comments were made in each section of the CSS `*/ /*` to assist with back end readability.

`<div class="hero">` was renamed `<section class="hero">` and moved to its own line.
  
After the `<header>` and `<section class="hero">`, the mockup had two clear columnns -- previously named `<div class="content">` and `<div class="benefits">`; these were changed to section class="conetnt" and `<section class="benefits">` for improved html semantics.
 
I tested all the `<nav>` and `<a>` links and not all of them worked, so I changed `<div class="search-engine-optimization">` to `<div id="search-engine-optimization">` activating the hyperlink `<a href="#search-engine-optimization"> Search Engine Optimization</a>` within the `<nav>` section of the `<header>`.


## MY APPROACH:

I knew I needed to clean up the `index.html` and the `style.css` sheets, but I didn't want to lose the original source code, so I copied each document and kept the SOURCE copy as a reference point. Anytime I got stuck or wanted to compare versions within my browser, I opened the code to live server. Often before comitting changes within the new `index.html` or `style.css` documents, I would use Chrome DevTools to "play in the sandbox" so to speak.

I also used a notebook and pencil to write down possible changes so I could check them off once I attempted them in the sandbox. Once I felt good about a change, I made a change to the index.html and/or style.css file(s), and ran the commands using Bash to add, commit, and push my changes to GitHub. Using pencil and paper helped ensure that my thoughts were followed through (cheks and balances), especially since I navigated back and fourth making changes between the files.

Lastly, I toggled between the `index.html` and the `SOURCE-index.html` in my web browser to ensure that the end result of the project followed the mockup and provided better accessibility within the web browser and on the back end for other developers.


## IMPLIMENTATION:

I used a top-down approach with the `index.html` sheet and did the same with `style.css`. Any time I made a change to either document I checked to see how it affected the function and appearance on the browser. Cleaning up meant adding comments, improving html semantics (putting `<h1>, <h2>, <h3>` in the correct order), and reducing redundant `style.css`.

When my finished version looked and acted the way the provided mockup did, I moved on to accessibility within the documents, adding `<alt="">` descriptions for images within the `<content>` and `<benefits>` sections. *After researching on the internet I determined that the banner image used in the hero section did not require an alt image as it is decorative. An argument can be made that the icon elements used in the second column do not require alt text and could have listed alt="" with empty brackets.*

## LESSONS LEARNED:

The most difficult part of the project for me was setting up the GitHub repository. Cloning the SSH from GitHub proved the be the most effective way of creating an effective remote relationship between my PC and the repository. At first I tried creating the project folder from my command line using mkdir, but accidently created the folder in the root fild/users location. The error I got from the command line prompted me to start over from within the `projects` folder from inside my `Desktop`. 
Subsequently, I learned that deleting files from a repository is messy work and can sometimes break relationships within a diretory, so I needed to git clone my repo then practice another git push with finalized changes, including a renaming of the files I wanted to keep, and removing files fromt the directory that were extraneous such as `run-buddy.html` which was used as a reference, and a random `.md` file that was created by a few quickly typed keystrokes.

## PROBLEMS SOLVED: 

Positioning of column two was a bit of a pain, but after I made sure that `.content {}` for column one was set to `position: relative;` `.benefits {}` were mostly accurate. I made sure to put `.benefits` AFTER `.content div {}` to allow the flow of the CSS to work properly. Stated another way, the hmtl for `<section class="content">` came before `<section class="benefits">` so I knew CSS needed to follow this model too.
  
## CODE IMPROVEMENT AND PERFORMANCE:

My `style.css` sheet is now only 148 lines long, whereas the `source-style.css` sheet was 200.

I wanted to clean up the appearance of the second column `<section class="benefits">`, so I adjusted the `padding` from `20px` to `16px` which affected the bottom margin of the content box within the `<section class="benefits">` allowing the column to align with the appearance of the `<section class="content">`.

If I were to talk with the client, I would ask if they like how the banner on the right side of the screen is displayed. Personally I think the spacing between elements could be improved, but I want to make sure and deliver the project to spec.

*Also, I would like to modify the file in CSS to display more properly within a mobile device or tablet; currently the website formatting works best on a desktop computer. Once I know how to make this improvement [something tells me to use a viewport...] I will update the file for full functionality. (11/23/2021)*

## Installation

Visit [@crosenfrisk on GitHub](https://github.com/crosenfrisk/horiseon/) to download the project 'horiseon' to your local device. Using the `<CODE CLONE>` button on GitHub, copy the SSH or HTTPS key and then use the command line prompt within **Git Bash $** git clone https://github.com/crosenfrisk/horiseon.git [and hit enter], this should save the file locally to your device.

## Usage

After downloading the project from GitHub to your local device, open the `horiseon` repository in a code editor such as Visual Studio Code, then view `index.html` in your web browser or Live Server.

## Credits

Conversations with cohort members :raised_hands: Kyler McLachlan and Megan Metelak :raised_hands: guided a few of the styling choices implemented in this project.
Connect with them on GitHub: @Kyler-Mclachlan, @Metelak.

### Articles from the Internet:

* [MDN: Accessiblility: CSS and JavaScript](https://developer.mozilla.org/en-US/docs/Learn/Accessibility/CSS_and_JavaScript)
* [W3Schools: Accessibility](https://www.w3schools.com/html/html_accessibility.asp)
* [Testing with Screen Readers](https://webaim.org/articles/screenreader_testing/)
* [Adding Alt Text](https://sc.edu/about/offices_and_divisions/digital-accessibility/guides_tutorials/alternative_text/adding-alt-text-ou-campus/banner_image_alt_text/index.php)

**Google Search: "what is an alt attribute in html"** provided good insight on where to use alt text -- in `<img>` elements in .html files moreso than .css files. Banners are *decorative* and can be skipped over by screen readers.

### Accessibility Tools:

* [Character Counter](https://wordcounter.net/character-count) to determine alt-text size, can type or copy paste. Helps to limit to 60 characters.
* [Accessibility Resources](https://cccaccessibility.org/assistive-tech/screen-readers)
* **Narrator** application within Windows 10 for PCs. 
* **VoiceOver** application within iOS for Mac, iPhones, and iPads.
* **TalkBack** Google's accessibility features for Android systems.


## License


##### *This is free and unencumbered software released into the public domain.*

##### *Anyone is free to copy, modify, publish, use, compile, sell, or distribute this software, either in source code form or as a compiled binary, for any purpose, commercial or non-commercial, and by any means.*


##### *In jurisdictions that recognize copyright laws, the author or authors of this software dedicate any and all copyright interest in the software to the public domain. We make this dedication for the benefit of the public at large and to the detriment of our heirs and successors. We intend this dedication to be an overt act of relinquishment in perpetuity of all present and future rights to this software under copyright law.*


##### *THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.*


##### *For more information, please refer to <https://unlicense.org>*
