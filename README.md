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
- The `grid-template-columns: repeat(auto-fit, minmax(280px, 1fr))` property enables the grid items to adjust dynamically to the available space, making the layout fully responsive without manual breakpoints.  
- Gap properties provide consistent horizontal and vertical spacing between items, improving readability and visual balance.  
- Max-width constraints are applied to prevent grid items from stretching excessively on wide screens, ensuring a clean and uniform presentation across devices.  
- CSS Grid works alongside Flexbox in other sections, giving precise control over both multi-column layouts and individual element alignment within the grid items. 

## Selectors and Pseudo-Classes
- **Selectors used:** element (`video`, `audio`), class (`.inline-group`), attribute (`input[type="radio"]`), descendant child (`>`), adjacent sibling (`+`)  
- **Pseudo-classes implemented:** `:hover`, `:focus`, `:checked`,`:active`,`:valid` 

## Animations, Effects, Transforms, and Transitions
- A carousel is implemented in about.html using `@keyframes` to slide images continuously, creating dynamic visual content.  
- Smooth `transition` effects are applied to buttons, links, and form elements for interactive hover feedback, improving user experience.  
- Box-shadows and border-radius are used on images, cards, and buttons to add depth and subtle visual layering.  
- Hover transformations scale images and change colors on interactive elements, providing clear visual cues for clickable items and enhancing engagement.  
- Overall, these animations and effects create a modern, polished, and responsive interface while maintaining usability and accessibility. 

## Accessibility Improvements
- All images include `alt` attributes.  
- Forms include associated `<label>` tags and proper input types.  
- Semantic HTML elements used for screen readers.  
- Color contrast adjusted for readability.  

## Cross-Browser Compatibility
- Tested on Chrome and Firefox  
- Flexbox and Grid layouts adjusted with `minmax` and `auto-fit` to ensure responsive behavior.  
- Iframes and media elements are responsive using `width: 100%` and `aspect-ratio`.    

## Viewing Locally
1. Clone or download the repository.  
2. Open the project folder.  
3. Open `index.html` in a browser to view the website locally.   

