# Paperframe motion

Use small, deliberate movements to make the paper-and-window interface feel responsive. Motion should clarify an action or a change of state, and stop when it has done its job. Apply it to web interfaces; a static poster does not need motion.

## Easing and timing presets

The first two curves and the duration ranges for controls, expanding indicators, and number reels are based on the captured BBKan website. The remaining timing choices are adaptable starting points for this skill, not claims about the original site's implementation.

| Preset | Curve | Typical duration | Use |
| --- | --- | --- | --- |
| Responsive | `cubic-bezier(.2,.8,.2,1)` | 180–220 ms | Button, hover, focus-adjacent, selection and indicator changes |
| Settle | `cubic-bezier(.16,1,.3,1)` | 350–850 ms | A quiet panel entrance or optional number reel |
| Exit | `cubic-bezier(.4,0,1,1)` | 120–180 ms | A dismissing panel, when the exit must be animated |
| Move | `cubic-bezier(.4,0,.2,1)` | 220–350 ms | A short movement between two known states |

Nonlinear easing means speed changes during the transition: responsive and settle start quickly and slow near the destination; exit accelerates as an element leaves. A cubic Bézier curve can be used directly in CSS, Web Animations API, or equivalent animation libraries.

## Apply with restraint

- **Controls:** change color, border, or a hard shadow in about 180 ms. A press may move a tactile control by 1 px; keep keyboard focus instantly visible and do not depend on hover for touch.
- **Indicators:** slide or resize an active marker over 220 ms. Mark selection with text or semantics as well as color.
- **Panels:** for a deliberate entrance, combine a short 4–8 px movement and opacity, finishing around 350 ms. The final, readable state must be present even when animation is unavailable.
- **Numbers:** optional reels may settle over about 850 ms. Keep the actual value accessible as text, hide purely decorative digits from assistive technology, and avoid replaying on every update.
- Avoid continuous loops, exaggerated overshoot, layout shifts, or motion on every card. Prefer `transform` and `opacity` for movement; never animate `transition: all`.
- Do not make core content initially invisible until JavaScript adds a class. If animation is used, make the visible final state the default, and opt in only when the application can trigger and complete it.

## Implementation and accessibility

Import [../assets/bbkan-motion.css](../assets/bbkan-motion.css) after the theme if using the optional utility classes. `bbkan-motion-control` only supplies transition timing: the host component owns hover, pressed, focus, and disabled styles. `bbkan-motion-enter` is an opt-in one-shot entrance. `bbkan-motion-indicator` transitions transform and opacity; the host owns those state values.

For `prefers-reduced-motion: reduce`, the utilities disable transitions and entry animation so the final state appears immediately. Apply equivalent handling to custom animations, reels, and JavaScript animation code; keep state changes understandable with no movement. Avoid overriding a host component's own transform: animate a wrapper or compose transforms deliberately.

Check pointer, keyboard and touch states; rapid reversal; narrow screens; and reduced-motion mode. A dismissed element must stop receiving focus when hidden, and focus must remain visible throughout an interaction.

