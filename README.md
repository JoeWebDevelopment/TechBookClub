# Frontend Mentor - Tech Book Club landing page solution

This is my solution to the [Tech Book Club landing page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/tech-book-club-landing-page-fZQidjHU73). I built the page to practice translating a Figma design into semantic HTML and responsive CSS while paying close attention to accessibility and maintainable layout decisions.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Accessibility](#accessibility)
  - [Continued development](#continued-development)
  - [AI collaboration](#ai-collaboration)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View an appropriate layout across mobile, tablet, and desktop screen sizes
- See hover and keyboard-focus states for interactive elements
- Navigate the page using semantic links and a logical heading structure
- Understand meaningful images and visual ratings through accessible text alternatives

### Links

- [Live site](https://darling-valkyrie-a5b896.netlify.app/)
- [Source code](https://github.com/JoeWebDevelopment/TechBookClub)

## My process

I began by structuring the complete page in HTML before focusing on visual styling. This helped me think through the document outline, section boundaries, lists, pricing-card headings, image alternatives, and the difference between links and buttons.

I then built the desktop layout section by section and adapted it for tablet and mobile widths. I used reusable layout classes for shared two-column sections and component classes for patterns such as calls to action, ratings, feature lists, membership cards, and social links.

During development, I relied heavily on Firefox DevTools. Flexbox overlays, computed styles, the accessibility tree, and temporary outlines helped me understand which element owned a spacing or alignment problem instead of guessing at fixes.

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox and wrapping flex layouts
- Responsive media queries
- Locally hosted variable fonts
- CSS counters
- CSS pseudo-elements
- Responsive and decorative image assets
- Accessible focus states and screen-reader-only content
- Firefox DevTools and Accessibility Inspector

The project does not require JavaScript. 

### What I learned

#### Translating visual effects into CSS

One of my biggest takeaways was becoming more comfortable using `::before` and `::after` for decorative details. I used pseudo-elements to create background glow effects, custom checkmark bullets, journey arrows, and the circle around the word “club.”

Using pseudo-elements allowed me to keep decorative content out of the HTML. This kept the markup more semantic and prevented screen readers from announcing visual elements that do not add meaningful information.

The background glows taught me how to establish a positioning context with `position: relative`, place a decorative layer with `position: absolute`, and clip oversized effects with `overflow: hidden`. I also learned to consider stacking order and pointer interaction so decorative layers do not cover or interfere with page content.

I independently created the circle and journey-arrow effects by breaking each design detail into smaller positioning and layering problems. This was a rewarding milestone because a few months earlier I would not have known where to begin.

#### Flexbox sizing and alignment

This project deepened my understanding of Flexbox's main and cross axes. When the membership cards changed from a row to a column, I learned that `flex-basis` began controlling height instead of width. Setting the mobile container to stretch its children and resetting the cards' flex behavior produced the intended full-width stack.

I also encountered inconsistent spacing in the feature list. The apparent padding was caused by `justify-content: space-between` distributing a different amount of free space on every list item. In another case, the generated checkmark was shrinking beside longer text. Debugging these issues taught me to inspect the size and alignment of each flex item rather than assuming that visible space comes from margin or padding.

#### Semantic lists and CSS counters

The reading journey is an ordered process, so I kept it as an `<ol>` while creating custom visual numbers with CSS counters. This let me preserve the meaning of the sequence while styling the numbers and connecting arrows to match the design.

#### Responsive spacing

I learned to distinguish between spacing owned by a section and spacing owned by a parent layout. Section padding controls breathing room inside a section's background, while `gap` controls the relationship between sibling elements. Thinking about which element owns the space made the layout more predictable across breakpoints.

### Accessibility

Accessibility was considered throughout the project rather than left until the end. I focused on:

- Maintaining one `<h1>` and a logical `<h2>`/`<h3>` hierarchy
- Using ordered and unordered lists where the content has list meaning
- Giving meaningful photographs concise alternative text
- Hiding decorative arrows, icons, patterns, and avatars from assistive technology
- Exposing each five-star rating once with screen-reader-only text
- Giving icon-only social links accessible names
- Providing visible keyboard-focus states for interactive elements
- Using the Firefox accessibility tree to confirm roles and accessible names

One important lesson was that an image does not need alternative text merely because it can be described. The decision depends on whether the image contributes information that is missing from the surrounding content.

### Continued development

In future projects, I want to continue improving:

- Mobile-first CSS organization
- Fluid typography and spacing with fewer fixed values
- Responsive decorative effects that rely less on pixel-specific offsets
- Consistent component and utility-class naming
- Testing at widths between common device breakpoints
- Keyboard, zoom, overflow, and cross-browser accessibility testing
- Making smaller, focused Git commits with clear messages

### AI collaboration

I used ChatGPT as a technical mentor during this project. I asked for conceptual explanations, accessibility reviews, and help diagnosing specific HTML, Flexbox, and responsive-layout problems. I remained the primary developer and wrote the implementation myself rather than asking AI to generate the completed page.

The most useful assistance involved learning how to investigate problems with DevTools. Instead of receiving a finished solution, I was guided to inspect computed styles, Flexbox axes, generated pseudo-elements, accessible names, and breakpoint behavior. As the challenge progressed, I became increasingly able to identify and implement effects independently, including the decorative circle, journey arrows, checkmark markers, and background glows.

This workflow helped me use AI as a debugging and learning partner while continuing to build my own problem-solving skills.

## Author

- Frontend Mentor - [@JoeWebDevelopment](https://www.frontendmentor.io/profile/JoeWebDevelopment)
- GitHub - [@JoeWebDevelopment](https://github.com/JoeWebDevelopment)
