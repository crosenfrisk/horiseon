# Horiseon Refactor Project

## Description

This repository (Refactor Horiseon) was created for a bootcamp challenge project. The original source code came from: coding-boot-camp/urban-octo-telegram . 

Our "client" Horiseon is a fictional marketing agency who has requested to have their code adjusted to meet accessiblility standards for websites and optimized for search engine performance.

WHAT I DID

To help with accessibility, I first looked at the index.html file, which I quickly noticed had a lot of redundant text. Inside the body it seemed like everything was a div. The original/source code can be referenced in a docuement I renamed SOURCE-index.html. 

I cleaned up the <head> and added a proper title which tells the user where they are, the "Home [page] - Horiseon" visable in the browser tab.

Within newly named header section, I noticed a span element within the <h1> element, which I removed ( .seo {} was also removed from the CSS). I have yet to discuss with the client what their intent was, but my concern was that any screen readers trying to introduce the h1 element to their reader/user may get caught up within the styling of the word. However, if the client prefers I can revert it to the previous style using the span element to seperate out SEO from HoriSEOn.
  
To help with readability of the index.html file, I added Comments to delineate sections and their purpose within the document.

I added <nav> elements which seemed a better description for screen readers and backend web users than simply div within the <header> section.
  
Header elements were renamed within the CSS document. Since there were no class attributes for header, we did not need .header {}. Subsequent .header {} styles were renamed to header {}. 

div class="hero" was renamed section class="hero" and moved to its own line.
  
After the header and hero section, the mockup had two clear columnns -- previously named div class="content" and div class="benefits"; these were changed to section class="conetnt" and <section class="benefits" for improved html semantics.
 
I tested all the <nav> <a> links and not all of them worked, so I changed div class="search-engine-optimization" to div id="search-engine-optimization" activating the hyperlink a href="#search-engine-optimization" Search Engine Optimization /a within the <nav> section of the header.




  
MY APPROACH:

I knew I needed to clean up the index.html and the style.css sheets, but I didn't want to lose the original source code, so I copied each document and kept the SOURCE copy as a reference point. Anytime I got stuck or wanted to compare versions within my browser, I opened the code to live server. Often before comitting changes within the new index.html or style.css documents, I would use Chrome DevTools to "play in the sandbox" so to speak.


IMPLIMENTATION:

I used a top-down approach with the .html sheet and did the same with the .css. Any time I made a change to either document I checked to see how it affected the function and appearance on the browser. Cleaning up meant adding comments, improving html semantics, and reducing redundant css. When my finished version looked and acted the way the provided mockup did, I moved on to accessibility within the documents, adding alt="" descriptions for relative images.


I LEARNED:

PROBLEMS I SOLVED: 

Positioning of column two was a bit of a pain, but after I made sure that .content {} for column one was set to position: relative; .benefits {} were mostly accurate. I made sure to put .benefits AFTER .content div {} to allow the flow of the CSS to work properly. Stated another way, the hmtl for <section class="content"> came before <section class="benefits"> so I knew CSS needed to follow this model too.
  
HOW I IMPROVED CODE LAYOUT AND PERFORMANCE:

My style.css sheet is now only 148 lines long, whereas the source-style.css sheet was 200.

I wanted to clean up the appearance of the second column ("benefits"), so I adjusted the padding which affected the bottom margin of the content box within the <section class="benefits"> allowing the column to align with the appearance of the . content div {} elements or <section class="content">.

LINK TO APPLICATION:

You can see the site by visiting https://crosenfrisk.github.io/horiseon/


## Installation

This is a landing page, so nothing you need to install.


## Usage




## Credits

<!-- List your collaborators, if any, with links to their GitHub profiles.

If you used any third-party assets that require attribution, list the creators with links to their primary web presence in this section.

If you followed tutorials, include links to those here as well. -->


## License

<!-- The last section of a good README is a license. This lets other developers know what they can and cannot do with your project. If you need help choosing a license, use [https://choosealicense.com/](https://choosealicense.com/) -->


---

🏆 The sections listed above are the minimum for a high-quality README, but your project will ultimately determine the content of this document. You might also want to consider adding the following sections.

## Badges

![badmath](https://img.shields.io/github/languages/top/nielsenjared/badmath)

Badges aren't _necessary_, per se, but they demonstrate street cred. Badges let other developers know that you know what you're doing. Check out the badges hosted by [shields.io](https://shields.io/). You may not understand what they all represent now, but you will in time.

## Features

If your project has a lot of features, consider adding a heading called "Features" and list them there.

## Contributing

If you created an application or package and would like other developers to contribute it, you will want to add guidelines for how to do so. The [Contributor Covenant](https://www.contributor-covenant.org/) is an industry standard, but you can always write your own.

## Tests

Go the extra mile and write tests for your application. Then provide examples on how to run them.

---
© 2021 Trilogy Education Services, LLC, a 2U, Inc. brand. Confidential and Proprietary. All Rights Reserved. -->

<!-- # 01 HTML, CSS, and Git: Code Refactor

One of the most common tasks for front-end and junior developers is to take existing code and refactor it to either meet a certain set of standards or implement a new technology. Web accessibility is an increasingly important consideration for businesses, ensuring that people with disabilities and/or socio-economic restrictions have access to their website. Accessible websites are better optimized for search engines, and help companies avoid litigation.

For this week's Challenge, your task is to refactor an existing webpage to make it accessible and to improve SEO. It's important to follow the Scout Rule when working with an existing codebase: Always leave the code a little cleaner than you found it. 

To impress the imaginary client for this Challenge, you should go the extra mile and improve their codebase for long-term sustainability. Ensure that all links are functioning correctly and clean up the CSS to make it more efficient, such as by consolidating CSS selectors and properties, organizing them to follow the semantic structure of the HTML elements, and including comments before each element or section of the page.

Remember when working with a client, it is essential to read the acceptance criteria for guidance and clarity on what the client expects, especially when asked to make a judgment call, such as when an icon needs an accessible alt tag and when it is okay to leave it blank. 

To successfully complete this week's Challenge, all acceptance criteria must be fully addressed!

## User Story

```
AS A marketing agency
I WANT a codebase that follows accessibility standards
SO THAT our site is optimized for search engines
```

## Acceptance Criteria

```
GIVEN a webpage that meets accessibility standards
WHEN I view the source code
THEN I find semantic HTML elements
WHEN I view the structure of the HTML elements
THEN I find that the elements follow a logical structure independent of styling and positioning
WHEN I view the icon and image elements
THEN I find accessible alt attributes
WHEN I view the heading attributes
THEN I find that they fall in sequential order
WHEN I view the title element
THEN I find a concise, descriptive title
```

## Review

<!-- You are required to submit the following for review:

* The URL of the deployed application.

* The URL of the GitHub repository. Give the repository a unique name and include a professional README describing the project.

- - -
© 2021 Trilogy Education Services, LLC, a 2U, Inc. brand. Confidential and Proprietary. All Rights Reserved. -->
