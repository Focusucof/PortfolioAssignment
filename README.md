# INFR3120 Assignment 1: Devin Boodoo | Portfolio Website

- **Live site:** https://focusucof.github.io/PortfolioAssignment/
- **Repository:** https://github.com/Focusucof/PortfolioAssignment

## Pages

| File | Purpose |
|---|---|
| `index.html` | Home page with navigation and a short introduction |
| `about.html` | Photo, introduction and embedded video |
| `projects.html` | 4 of my personal projects, each with an image, heading, short description, and link to the project |
| `contact.html` | Contact form with validation (name, email, phone, message) |

## Project Structure

```
css/
  full.css      (laptop / desktop)
  tablet.css    (tablet)
  mobile.css    (mobile)
images/         (profile photo and project logos)
index.html
about.html
projects.html
contact.html
README.md
```

## Semantic HTML

I used semantic HTML to separate different sections of the HTML file through all 4 pages.

| Tag | Where I used it | Why |
|---|---|---|
| `<header>` | At the top of all four pages | Holds the logo and the main navigation |
| `<nav>` | Inside the header on all four pages | Holds the navigation links for the site |
| `<main>` | Once on each page | Wraps the content that is unique to that page, so it stays separate from the header and footer |
| `<section>` | Projects and contact pages, and the two groups of text on the About page | Groups related content together |
| `<article>` | The About page | I had a block of text with separate paragraphs and headings so I put it all within the \<article> tags |
| `<footer>` | The bottom of all four pages | Holds the copyright notice |

I also used `<div class="container">` to set the minimum page height so the footer appears where it's supposed to

## Responsive Design (Viewports)

Each page loads the appropriate CSS file with the media attribute in the link tag. There are 3 CSS files, 1 for full sized displays, 1 for tablets, and 1 for mobile.

| Viewport | CSS file | Width range | Why this size |
|---|---|---|---|
| Mobile | `css/mobile.css` | up to 480px | Most phones are around 480px. This is also a key point where elements that were very long should be getting stacked or else they won't render properly |
| Tablet | `css/tablet.css` | 481px to 959px | This range covers tablets sized screens. Here I reduced the margins and made text slightly smaller so that less space is wasted |
| Laptop | `css/full.css` | 960px and up | 960px is where a full sized layout fits, so everything from here up uses the roomier layout with the content kept at 60% width so lines of text don't get too long and everything can be focused in the center. |

What changes between sizes:

| Item | Mobile | Tablet | Desktop |
|---|---|---|---|
| Content width | 100% | 80% | 60% |
| Main heading size | 2.25rem | 3.5rem | 5rem |
| Navigation links | smaller text and padding | medium | full size |
| Project cards | image above text | image beside text | image beside text |

## Gradients

- **Linear gradient:** the navigation bar on every page uses `linear-gradient(to top, #101010, #2c2c2c)`.
- **Angle linear gradient:** each project card on `projects.html` uses `linear-gradient(45deg, #101010, <card colour>)`, with a different colour for each card (see the colour table below).

## Colour Palette

Generated with Adobe Color using the Complementary rule, with #E9D3B6 as the base colour.

| Colour | Where it is used |
|---|---|
| #E9D3B6 (Base Colour) | Highlighted heading words (e.g. "Boodoo", "Me") and the Send button on the contact form |
| #B5D6E8 | Gradient on the first project card |
| #658393 | Gradient on the second project card and the highlighted words in the About page text |
| #A89882 | Gradient on the third project card |
| #695336 | Gradient on the fourth project card |

Adobe Color link: https://color.adobe.com/create/color-wheel?color-palette=E9D3B6%2CB5D6E8%2CA89882%2C658393%2C695336&color-palette-name=My+Color+Theme

Black, white and greys (#101010, #2c2c2c, #1f1f1f and #fff) are used as neutral backgrounds, borders and text.

## Contact Form Validation

The form uses HTML5 validation for each field:

- `required` on name, email, phone and message
- `type="email"` to check the email format
- `type="tel"` for the phone number
- `maxlength="500"` on the message
- `action="mailto:..."` with `method="post"` and `enctype="text/plain"` to send the form through an email client

## Testing and Validation

| Check | Tool | Result |
|---|---|---|
| HTML | W3C Markup Validator (https://validator.w3.org/) | 0 Errors |
| CSS | W3C CSS Validator (https://jigsaw.w3.org/css-validator/) | 0 Errors |
| Links | W3C Link Checker (https://validator.w3.org/checklink) | 0 Errors |
| Spell Check| Datayze (https://datayze.com/website-spell-checker) | Only flagged my name, acronyms, and names of my projects|
| Accessibility | WAVE (https://wave.webaim.org/) | 0 Errors |

## Version Control and Deployment

- Code is stored in a public GitHub repository, with commits made after each major change.
- The site is deployed with GitHub Pages from the `main` branch.

## Sources and Citations

- Code structure for the video, form and CSS follows code shown in lecture.
- Font: JetBrains Mono from Google Fonts: https://fonts.google.com/specimen/JetBrains+Mono
- Colour scheme: Adobe Color: https://color.adobe.com/create
