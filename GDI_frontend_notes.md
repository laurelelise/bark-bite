#GDI HTML2 CSS2 workshop

Notes from Girl Develop It course on Feb 27th, 2016. Plus added notes from research and building a website for a friend. 

##Standard Practices

1. Reset CSS files
When you're designing for the web, there are different defaults for various browsers(chrome, safari, opera and IE *ugh in specific circumstances like big corps and non profits*). Keep in mind, it's tricky to get a page to look the same across every browser. So the reset.css contains all the rules to zero everything out. It will give default sizing to all your tags—awesome. It makes an even playing field for each browser. Examples of "normalizing" inconsistencies include:
 - lists
 - paragraphs
 - links

 *Note that when you're using CSS you can specify multiple styles for each element.*

2. Standard widths and sizes
- All screen sizes vary so content needs to be wrapped in containers to control minimum and max width to stretch. Font sizes will vary by screen size.
- Retina screens are higher resolution screens with double the pixel density, so in this case it's 150 dots per inch. You can add a script that detects if the user has a Retina screen.(more on that later)
- Fixed width is the same size no matter what screen your user is looking at: 960 to 1280 is fixed width.
- Fluid width is set to a percentage of the available screen. It's also referred to as a liquid layout: it will always take up the same amount of size on the screen so it scales down. The majority of the components have percentages for the width and the layout adjusts for the width based on the users screen size.

3. Containers for layout
- Wrappers are a good way to center all the content if the screen is wider than your content
- Unless you specify, the container is going to take up 100% of the screen width.

Take a look at the example below that shows a centered container:

```CSS2
.container {
     width: 100%; /* take up full viewport width */
     max-width: 1400px; /* if viewport is larger than 1440px,
                           don't let it take up 100% */
     margin: 0 auto; /* center content in the viewport */
 }
 ```

###HTML5
 It's a collection of the latest W3C web technology that includes CSS, HTML and JS. http://caniuse.com/ Allows you to look up all the HTML5 elements by the browser type.
 - It marks some things obsolete as "depreciated" where it may not show properly in a browser
 - Use strong and emphasize tags to be more descriptive about text, this allows for better SEO and semantic coding
 - Here's a list of all the obsolete tags: https://www.w3.org/TR/html5/obsolete.html
 - Separate presentation from the type of content
 - Doctype has to be a part of every website which used to be a very long tag that specifies the type of html you're using.
####There are new structure elements.
Now divs are considered an older method of structure. With HTML5 you will use the following tags:
- <section> tags which will group together thematically related content. It's similar to the div tag but better because it's semantic
- <header> element allows you to have multiple headers per page. ie. if you have multiple headers for a blog post. It's used for a group of introductory text like logo/tagline or nav aids.
 - <nav> element  accepts a list of links for your navigation and lives in the header. You can put a secondary nav in the footer element.
 - <footer> copyright info, secondary nav, you can create multiple footers per page.
 - <aside> can be anything that's tangentially related to the information in the main content, like a sidebar or pull quotes, widgets in wordpress are aside elements
 - <article> is a single story on a website that's self-contained. It's loosely translated but it could be a forum post, reviews, blog

## Horizontal Fixed Nav
Allows users to have access to navigational elements all the time because the bar at the top stays fixed while you dive into the body content.  The only thing to watch out for, is that it reduces the visible content on smaller screens. So if you have an "above the fold" image it might get cut off.


## Hero images
Large banner image that used as an "above the fold" attention grabber for your users. The first visual that a visitor encounters when they visit the website is the hero image. It's often image and text and it can be static or dynamic.
