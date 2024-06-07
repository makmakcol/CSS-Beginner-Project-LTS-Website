# 🌮The Little Taco Shop CSS Redesign🌮

## ✨About✨

This project is the final project in Dave Gray's "CSS tutorial for beginners" and is chapter 24 of the course. It starts with the HTML code from Dave Gray's previous "HTML tutorial for beginners" and overhauls the design of the site with modern CSS.

## ⚡️Key Features⚡️

- Menu: HTML table elements are converted to CSS grid.
  ```css
  /* || MENU */

  thead, 
  tbody, 
  tfoot, 
  tr {
    display: contents;
  }

  .menu__container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-template-areas: "hd1 hd2 hd3"
                          "cr cr1 cr1p"
                          "cr cr2 cr2p"
                          "cr cr3 cr3p"
                          "sf sf1 sf1p"
                          "sf sf2 sf2p"
                          "sf sf3 sf3p"
                          "cs cs cs";
    gap: 0.1em;
    margin-bottom: 1em;
  }

  .menu__cr {
    grid-area: cr;
  }

  .menu__sf {
    grid-area: sf;
  }

  .menu__cs {
    grid-area: cs;
  }

  .menu__cr, 
  .menu__sf,
  .menu__cs,
  .menu__header {
    color: var(--HIGHLIGHT-COLOR);
    font-weight: bolder;
    height: 100%;
    display: grid;
    place-content: center;
  }

  .menu__header,
  .menu__item {
    width: 100%;
    padding: 1em;
    border: medium ridge var(--BORDER-COLOR);
  }

  .menu__item {
    display: grid;
    place-content: center;
  }
- Hero: CSS animation is applied to the initial welcome message when the site first loads (lines 177 through 209).
- Responsive Design: With the use of modern CSS, minimal media queries are needed as the site responds to both large and small screens (lines 361 through 376).
- Light/Dark Mode: Both light and dark mode are featured in this project. The preferred method is set to dark mode in the media query (lines 62 through 79).
- JavaScript Functions: A touch of JavaScript has been added to update the year of the copyright.
  ```javascript
  const year = document.getElementById("year")
  const thisYear = new Date().getFullYear()
  year.setAttribute("datetime", thisYear)
  year.textContent = thisYear
- BEM Methodology: Block Element Modifiers methodology is applied to the CSS and HTML to keep the code structured and organized.
- ABCSS: Alphabetical organization of custom variables is applied for readability.

## 💡How To Run💡

1. Fork this repository.
2. Open the files in your code editor of choice (I use VS Code).
3. Install the extension "Live Server" by Ritwick Dey.
4. Click "Go Live" and the website will be viewed in your browser.

## 🔗Resources🔗

- [Dave Gray's CSS Complete Project for Beginners](https://www.youtube.com/watch?v=cMN2Odm5ieA&list=PL0Zuz27SZ-6Mx9fd9elt80G1bPcySmWit&index=25)
- [Dave Gray's HTML5 Website Project for Beginners](https://youtube.com/watch?v=T5PD8ofhiug)



 
   
