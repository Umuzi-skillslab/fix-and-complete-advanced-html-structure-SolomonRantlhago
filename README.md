# Media Production Website – Capstone Project

## Overview
This website is designed to showcase a media production company’s services, including video production, audio recording, and multimedia solutions. Users can view portfolios, explore media content, read client testimonials, and contact the company via a fully functional form. The site emphasizes responsiveness, accessibility, and modern web design practices.

## Issues Found
The starter code contained multiple HTML and CSS issues, including:

- Heavy reliance on `<div>` elements instead of semantic HTML5 elements (`<header>`, `<nav>`, `<main>`, `<section>`, `<footer>`).  
- Missing metadata (`<meta charset>`, `<meta viewport>`, `<meta description>`), affecting SEO and mobile responsiveness.  
- Images lacked `alt` attributes, reducing accessibility.  
- Forms were poorly structured: incorrect input types, missing validation, no `<fieldset>` grouping, and absent radio buttons, checkboxes, and dropdowns.  
- CSS issues: no Flexbox or Grid layouts, poor color contrast, missing media queries, and spelling errors flagged by stylelint.  
- Missing or incomplete media elements (video and audio), gallery images, testimonials semantic markup, and iframe responsiveness.  
- Validation errors: missing `lang` attribute, improper character encoding, and multiple accessibility violations.
- Advanced Features Missing: Animations, transitions, text effects and interactive elements absent. 

## Fixes and Implementations
- Replaced generic `<div>`s with semantic elements for proper structure.  
- Added essential metadata for charset, viewport, and description.  
- All images now include descriptive `alt` text.  
- Forms rebuilt with correct input types, `<fieldset>` grouping, required attributes, and client-side validation.  
- Videos and audios embedded properly with multiple source formats and responsive sizing.  
- Testimonials updated with `<figure>` and `<figcaption>` markup.  
- CSS reorganized, including media queries for responsiveness.  
- Flexbox and CSS Grid layouts were implemented to improve the layout, responsiveness, and overall user experience (UX).  
- Advanced features added include carousels, hover effects on buttons and links, smooth transitions, box-shadows, and animations to enhance interactivity and UX.

## Flexbox Layouts
- Form sections across the website use Flexbox to align labels with inputs, checkboxes, and radio buttons. This ensures that form elements are consistently spaced and visually aligned both horizontally and vertically, improving readability and user experience on all screen sizes.  
- The navigation menu, testimonial section in media.html, and services section in about.html utilize Flexbox for flexible horizontal layouts. Flex-wrap is applied to allow elements to automatically move to the next line on smaller screens, maintaining responsiveness and preventing layout breakage.  
- Flexbox was also used to center content vertically within sections, such as headings and images, providing a balanced and polished design without relying on fixed margins or manual spacing.  

## CSS Grid Layouts
- The offerings section in index.html and the video-showcase section in media.html utilize CSS Grid to create flexible multi-column layouts, allowing multiple items (services, videos) to be displayed side by side on larger screens and stacked neatly on smaller screens.  
- The `grid-template-columns: repeat(auto-fit, minmax(250px, 1fr))` property enables the grid items to adjust dynamically to the available space, making the layout fully responsive without manual breakpoints.  
- Gap properties provide consistent horizontal and vertical spacing between items, improving readability and visual balance.  
- Max-width constraints are applied to prevent grid items from stretching excessively on wide screens, ensuring a clean and uniform presentation across devices.  
- CSS Grid works alongside Flexbox in other sections, giving precise control over both multi-column layouts and individual element alignment within the grid items. 

## Selectors and Pseudo-Classes
- **Selectors used:** element (`video`, `audio`), class (`.inline-group`), attribute (`input[type="radio"]`), descendant child (`>`), adjacent sibling (`+`),`:not()` 
- **Pseudo-classes implemented:** `:hover`, `:focus`, `:checked`,`:active`,`:valid`, `:required`, `:disabled`, `:nth-child()` 

## Animations, Effects, Transforms, and Transitions
- A carousel in about.html uses `@keyframes` to slide images with a back-and-forth effect using `animation-direction: alternate`. 
- Smooth `transition` effects on buttons, links, and cards for interactive hover feedback.
- Service cards use `rotateX(5deg)` with `perspective` for a 3D top-down fold effect on hover.
- The submit button uses `skewX(-1deg)` and `scale(1.02)` on hover.
- `@media (prefers-reduced-motion: reduce)` added to respect users with motion sensitivity, disabling all animations and transitions.
- Box-shadows and border-radius add depth and visual layering throughout. 
- All animations and effects are demonstrated in the website demo videos located in the `screenshots/` folder.

## Accessibility Improvements
- All images include `alt` attributes.  
- Forms include associated `<label>` tags, proper input types, and `aria-describedby` attributes for screen reader support. 
- Semantic HTML elements used throughout for screen reader compatibility.
- `.sr-only` class implemented to provide screen-reader-only text where needed.
- `aria-label` added to navigation and form elements.
- Color contrast adjusted for readability across all pages.

## Cross-Browser Testing & Debugging
- Tested on Google Chrome and Microsoft Edge.  
- All four pages rendered consistently across both browsers with no layout differences or visual issues detected.
- Mobile testing was performed using the browser DevTools Inspect tool to simulate mobile screen sizes, confirming that all responsive layouts and media queries work correctly on small screens.

### W3C Validation
- All four HTML pages were validated using the Nu HTML Checker with no errors or warnings on any page.
- styles.css was validated using the W3C CSS Validation Service and passed with no errors (CSS Level 3 + SVG).

### Issues Found and Fixed During Debugging
**Errors in the original starter files (identified via W3C validation):**
- All four HTML pages were missing the `lang` attribute on the `<html>` tag. This was flagged as a warning by the validator. Fixed by adding `lang="en"` to all pages.
- All four HTML pages were missing `<meta charset="UTF-8">`, causing the validator to fall back to `windows-1252` encoding. Fixed by adding the charset meta tag to all pages.
- Images in about.html (work1.jpg, work2.jpg, work3.jpg) and media.html (client1.jpg, client2.jpg) were missing `alt` attributes, flagged as errors by the validator. Fixed by adding descriptive `alt` text to all images.

## Screenshots
Screenshots and demo videos are located in the `screenshots/` folder, including:
- All four pages on desktop view (Chrome and MS Edge)
- index.html and contact.html on mobile view
- W3C HTML and CSS validation results
- Same pages in Chrome and Microsoft Edge for browser compatibility
- Form validation messages in action
- Website demo videos showing animations and effects in action across all four pages
- Video, audio, and iframe elements functioning
- Flexbox and CSS Grid layout demonstrations

## Code Quality & Linting
- The CSS stylesheet is organised into clearly labelled sections with 
  comments separating styles for each page (index.html, about.html, 
  contact.html, media.html, and generic/shared styles).
- Consistent naming conventions are used throughout, with class names 
  reflecting their purpose (e.g. `.form-group`, `.offering-grid`, 
  `.testimonial-grid`).
- No duplicate or redundant CSS rules remain in the final stylesheet.
- All HTML files follow consistent indentation and structure, with 
  semantic elements used in place of generic `<div>` containers.
- W3C validation was used as a quality gate — all four HTML pages and 
  the CSS file passed with zero errors before submission.

## Known Issues and Limitations
- The image carousel in about.html is CSS-only and does not include manual navigation controls, meaning users cannot skip to a specific slide.
- Videos and audio files are stored locally and will not play if the project is viewed without the media files present in the correct folder.

## Reflection
The main challenges faced during development included:

- Structuring the CSS file cleanly across four pages without duplication required careful planning and section comments to keep related rules grouped.
- Implementing the 3D `rotateX` effect on service cards required understanding `perspective`, `transform-style: preserve-3d`, and `transform-origin` together, as the effect did not work correctly until all three were applied on the right elements.
- The Google Maps iframe sandbox issue was unexpected — it appeared to add security but the W3C validator flagged it as counterproductive. Researching the issue led to a better understanding of how sandbox attributes interact.
- Balancing the `@media (prefers-reduced-motion)` rule with existing animations required understanding how `!important` overrides work in CSS

## Viewing Locally
1. Clone or download the repository.  
2. Open the project folder.  
3. Open `index.html` in a browser to view the website locally.   

