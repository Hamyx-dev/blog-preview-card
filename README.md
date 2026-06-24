# Blog Preview Card

This is what I built for the assignment to recreate a blog preview card design using only HTML and CSS, no JavaScript and no AI generated code.

## What I Built

I built a card that shows a category badge, a publish date, a heading, a paragraph and an author section with an avatar and a name. The card also has an entrance animation, a gradient background on the page and a circle avatar.

## The HTML Structure

I used article for the whole card because the instructions said to use semantic elements, and an article is a piece of content that can stand on its own, which a blog preview card is. Inside the article I have an image, a span for the category badge, a p with a time element inside for the publish date, an h2 for the heading, a p for the description, and a footer for the author section.

I learnt that time needs a datetime attribute written in a proper date format, even though the text you actually see on the page can be written in a normal way like 23 June 2026. The datetime attribute is for machines to read and the text inside is for humans to read.

I also gave both my images proper alt text instead of leaving it empty, because empty alt text does not describe anything to someone using a screen reader.

## The CSS

### Centering

I used flexbox on the container with justify-content and align-items both set to center, and height 100vh so it fills the whole screen.

### The card

I gave the card a fixed width and height, rounded corners with border-radius, and a box-shadow for depth.

### The entrance animation

This was the bonus part I found hardest at first. I learnt that keyframes cannot be written inside another rule like .card, it has to be its own separate block on its own, starting with @keyframes and a name I choose myself. Inside the keyframes I wrote a from state where the card has opacity 0 and is shifted down a little with translateY, and a to state where opacity is 1 and translateY is back to 0. Then on the .card rule itself I added an animation property that calls that keyframes name, with a duration, a timing function and forwards so it stays in its final state instead of jumping back.

I learnt that the name I give the keyframes has to match exactly, spelled the same way, in both places, or the browser will not connect them and nothing will happen, with no error message at all.

### Gradient background

I changed the page background from one flat color to a linear-gradient going from my yellow color to a lighter, paler version of the same yellow, so it stays subtle instead of looking like two different colors fighting each other.

### Circle avatar

I gave the avatar image a border-radius equal to half of its width and height, which is what turns a square image into a perfect circle.

## Mistakes I Made and Fixed

1. I tried to write @keyframes inside the .card rule instead of as its own separate block, which is not valid CSS.
2. I forgot the s at the end of keyframes the first time.
3. I left a footer tag open without closing it, which made the next closing div tag close the wrong element instead.
4. My author name was sitting far away from the avatar image because of margin on all sides of the image instead of just the side that needed spacing.

## What I Learnt

I learnt that small CSS mistakes do not throw an error in the browser, the browser just quietly ignores the line that is wrong, which means you always have to check your work visually after every change instead of trusting that no error message means everything is correct. I also learnt that getting the HTML nesting right first makes every CSS decision after that much easier to reason about.