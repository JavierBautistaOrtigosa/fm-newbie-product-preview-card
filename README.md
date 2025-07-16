# fm-newbie-product-preview-card

/*Why width: auto isn’t stretching:
In flexbox, by default:
width: auto = “take up as much space as your content needs”, not “take all available space.”

How to make it fill remaining space:

Take all available width (horizontally)
Fix
Use flex: 1;
Goal
Stretch to parent's width
Fix
Use align-self: stretch; or set parent’s width */
