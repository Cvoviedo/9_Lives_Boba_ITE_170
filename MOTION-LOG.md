# Motion log

**Student:** Cameron Oviedo
**Shop name:** 9 Lives Boba
**Live site:** https://

## Motion sentences

Write one row for every animation. Fill in all six parts:

> When **[trigger]**, the **[element]** changes **[property]** over **[duration and delay]** with **[easing]**, so that **[job]**.


Jobs: feedback, orientation, continuity, status, storytelling, delight.

| # | Req | Trigger | Element | Property | Duration / delay | Easing | Job | Tool |
|---|-----|---------|---------|----------|------------------|--------|-----|------|
| 1 | R1 | Hover, focus, or press | Menu buttons and drink cards | Scale, box-shadow | 300ms | ease-out | feedback | transition |
| 2 | R2 |Page load | Headline words |Opacity and translateY| 900ms, staggered 120ms | ease-out| orientation | @keyframes|
| 3 | R3 | Page open| Cat's tail | Rotate -12° to 12° | 2s, infinite | ease-in-out | delight| @keyframes|
| 4 | R3 | Page open | Shop sign | Rotate -5° to 5°| 3s, infinite | ease-in-out | continuity | @keyframes |
| 5 | R4 | Scroll into view | Boba drink cards  | Opacity and translateY  | 600ms, staggered 100ms | ease-out | storytelling | IntersectionObserver |
| 6 | R5 | User scrolls through featured drink section | 9 Lives Boba image |Scale| Follows scroll progress (0–1) | ease-out | storytelling | Scroll progress |
| 7 | R6 | Click add to order | Add to order button | Scale | 500ms | ease-out | feedback | element.animate() |
| 8 | R6 | After button animation finishes| Cart counter | Scale | | ease-out | status | element.animate() |

Tool = transition, @keyframes, IntersectionObserver, scroll progress, element.animate(), SVG, View Transition.

## Easing choices (R7)

Name three different easing curves you used. For each, say in one sentence why it fits that motion.

1. ease-out: I used ease-out for my headline entrance because it starts quickly and then slows down smoothly, making the words feel like they are settling into place.
2. ease-in-out : I used ease-in-out for the cat's tail and swinging shop sign because it creates a smooth movement in both directions without making the animations feel rush.
3. ease-spring: I used this spring-like easing for the cart counter because the slight bounce feel playful and gives customers noticeable feedback when they add a drink.

## What I saw in the X-ray

Pick one animation and describe what the Motion X-ray or the Chrome Animations panel showed you that you couldn't see at normal speed.

I noticed that the progress bar in the Motion X-ray moved forward and backward because the cat's tail animation loops infinitely. I also noticed how the easing makes the tail swing smoothly instead of moving suddenly. Slowing it down helped me see how the tail changes direction.

## Checks

- [x] (R8) Reduced motion emulated in DevTools: what still moves, and what stops?
- [x] (R8) Pause button stops every infinite loop, and works from the keyboard
- [x] (R8) Every :hover effect also happens on :focus-visible
- [] (R8) Nothing flashes more than 3 times per second
- [x] (R9) Paint flashing checked: my animations use transform and opacity
- [x] (R9) No `transition: all` anywhere
- [x] (R4) With JavaScript disabled, every card is still visible
