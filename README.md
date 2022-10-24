# code-refactor-week1
Week 1 02-Challenge

## Link to Deployed Application...
https://pkrysinski.github.io/code-refactor-week1/


<div align="left">
    <img src="./assets/images/GitHub-project-screenshot.png" width="800px"</img> 
</div>

## Overview of the Challenge
-We've been given a sample webpage with redundant features, ambiguous div tags, and broken links.  Our goal is to
clean up the CSS, correct the issues in the HTML, and make sure the website is deployed appropriately.  Through
various iterations of code modifications and commits to the repository, I hope you can see the progress made along
the way to ultimately land at the cleanest version we can imagine of the website up until this point in class.  I'm
sure it can be done better, but ultimately I wanted to treat it like a campsite - leave it better than when we found
it.  Below are just some of the changes done, and validation of all acceptence criteria with rationale explaining
each change, and how I went about resolving it.  I hope you enjoy!

## CSS (extra) Changes so far...

Problem:
-The "Search Engine Optimization" interactive text/button in the header does not take you to the associated SEO 
section on the webpage like the other 2 buttons ("Online Reputation Management" & "Social Media Marketing" do).
The Solution:
-The body contains multiple divs with associated classes; one of which is "content" which contains the actual 
divs for information on the 3 content buttons in the header.  The 2 buttons that work have "id"s associated with them, 
so we need to add the appropriate id to the SEO button (in html) too.


Problem:
-The CSS file is not organized at all by page layout and area of interest in which the code is written for.  
Solution:
-I'm organizing it as best I can first in order of how they relate to things on the page (header classes + ID's 
up top, body in the middle, and footer towards the bottom) as best as I can.


Problem:
-The CSS file as a ton of redundant code which can definitely be consolodated.  The three classes in there for 
.benefit-lead, .benefit-brand, and .benefit-cost all have the same values.
Solution:
-Consolodating classes and ID's that contain the same property/value pairs into singular classes and ID's.  In this 
example, ".benefit-lead", ".benefit-brand", and ".benefit-cost" will now all be consolodated into a singluar h3 class, 
so that all h3's get reflected the same and there's less to manage.

## Acceptance Criteria

```
GIVEN a webpage meets accessibility standards
WHEN I view the source code.
THEN I find semantic HTML elements.
    -There are a lot of generic div tags in the HTML that if left alone, can be a little ambiguous from both an 
    accessibility standpoint and what the general purpose of the element is.  For example, the header tag is 
    currently a generic "div" tag.  As is the footer.  So we've replaced those with <header> and <footer> respectively. Also 
    within the main body, we've got sections, which we've renamed from <div> to <section>, so make more sense to whomever 
    is interpreting the website.  The right-float "benefits" section is also more of an aside than just a section like the rest, 
    so we'll name that accordingly.

WHEN I view the structure of the HTML elements.
THEN I find that the elements follow a logical structure independent of styling and positioning.
    -Structure of HTML elements have been organized to follow industry standards with correct HTML, Head, and Body tags with
    appropriate content matter inside of each, nested (hopefully) properly to also abide by industry standards.

WHEN I view the icon and image elements.
THEN I find accessible alt attributes.
    -Have added alt="" attributes to every image on the HTML to better describe what the image looks like when rendered 
    on the page.

WHEN I view the heading attributes.
THEN they fall in sequential order.
    -Switched "Online Reputation Management" with "Search Engine Optimization so that they fall in (alphabetically and 
    length of content) sequential order.
        1. Online Reputation Management
        2. Search Engine Optimization
        3. Social Media Marketing
    -Since we ordered the list in the header alphabetically, it only makes sense to order the content alphabetically.  I've 
    re-ordered the divs in the "content" area of the body to follow the same alphabetical order, and changed the image floats 
    to keep the integrity of the initial website.
    -^This is how I interpreted it at first, but now seeing Amy and Sada's messages in Slack, I noticed that the .CSS needs 
    some organization, and indeed the h1, h2, and h3 aren't in sequential order in there either, so I cleaned them up and 
    organized the css code to hopefully also reflect the request for sequential order there too.

WHEN I view the title element.
THEN I find a concise, descriptive title.
    -Changing title from "website" to "© Horiseaon"

```