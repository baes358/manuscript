# Typography & Interaction Project 1

This project was created for my Typography & Interaction course at Parsons. It presents Kristen Coogan's article "Knowing Your Design History is Crucial to Aesthetic Innovation" alongside my personal response, exploring how historical fluency in design shapes one's contemporary creative practices.

## Chosen Reading

The base article is Kristen Coogan's piece from AIGA Eye on Design, which examines style as a cycle. Lorraine Wild's "Great Wheel of Style" is a framework that essentially shows how design trends cycle from high culture to mass market, before revival brings them back as "good design" again.

## HTML Structure

The major elements used:

- `<header>` — Site header with article title, publication source, and author
- `<nav>` — Internal navigation linking to Article, Response, and About sections
- `<main>` — Contains both the article and response content
- `<article>` — Two articles: one for the reading, one for my response
- `<section>` — Divides content into thematic chunks (Miranda's Lesson, A Wheel of Style, Revival & Renewal, etc.)
- `<blockquote>` with `<cite>` — Styled pull quotes highlighting key passages
- `<aside>` — Supplementary notes providing context
- `<footer>` — Navigation links and copyright

- `<em>`, `<strong>`, `<span>` — Emphasis and highlight for body paragraph texts

## CSS Formats

### reset.css
A modern CSS reset derived from [the-new-css-reset](https://github.com/elad2412/the-new-css-reset). 

### style.css

**Custom Properties (CSS Variables)**
```css
--off-white: #FFF1F4;
--off-black: #2E2D2D;
--dusty-rose: #874f6d;
--dark-pink: #b31e68;
--mid-pink: #ed72b0;
--pink: #ffd2f6;
--light-pink: #fbddf4;
```

**Typography**
- Two custom `@font-face` declarations: Philibert (display/headings) and National Park(body)
- Headings use Philibert with decorative double quotes as pseudo-elements (`::before` and `::after`)
- Body text uses National Park at 1.1rem with readable line-height (1.75rem)

**Layout & Responsiveness**
- Flexbox-based layout with `flex-direction: column` on `<main>`
- Three breakpoints using modern CSS media queries:
  - Mobile: default styles
  - Tablet (790px–1100px): 40rem content width
  - Desktop (>1100px): 50rem content width

**Visual Design**
- Gradient backgrounds on section headers (dark pink to pink for article, black to gray for my response)
    - Different visuals compared to old design, but still keeping similar themes in terms of layout, color, sizing
- Dashed borders for section separation
- Blockquotes with left border accent and contrasting background
- Asides with dashed stroke
- The response section inverts the color scheme (dark background, light text)

**Animation**
I used the marquee effect visualizes Wild's "Great Wheel of Style":
```css
@keyframes marquee {
  0%   { transform: translateX(0); }
  100% { transform: translateX(-50%); }
}
```
- Infinite horizontal scroll at 25s duration for speed control
- Pauses on hover via `animation-play-state: paused`
- Duplicated list items to create seamless looping and no breaks

## Design Decisions

The typefaces I chose for this revision are slightly different. I kept Philibert and added National Park as they both have subtle, minor inconsistencies that reflect how I feel about history. The  pink-and-off-white palette for the article transitions to a darker gray scheme for my response, and it functions to visually distinguish the original text from my personal reflection.

The marquee animation isn't just a decorative element, as it displays the cyclical nature of style that Coogan describes, looping endlessly from "Good Design" to "Revival", and repeated infinitely.

## Lessons Learned

- Semantic HTML improves a website's accessibility, SEO, and long-term maintainability (and it is easier to read organized structures)
- Keep one `<h1>` per page and use `<h2>`/`<h3>` for structured hierarchy when needed
- CSS custom variables/properties make theming and color adjustments much easier
- The reset stylesheet should load *before* custom styles
- Writing a README documents what the project is, how it was built, and why it matters

## Future Improvements

- Add scroll-based animations or parallax effects
- Implement different layout structures using grid, especially at different viewport dimensions
- Explore additional interactive elements that can express the "wheel of style" concept
