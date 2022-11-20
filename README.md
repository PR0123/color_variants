# The idea

Light and dark interfaces use very different color palettes. And so instead of fixed colors we can use semantic colors, but the list of adaptive colors will always be limited.

Assuming initially I use color in the light palette I would like to get corresponding dark color for every RGB color. And symmetrically, to get light counterpart for every color in the dark palette. Is there currently a better way than manually defining infinite number of colors in the asset catalog?

From a design perspective, wouldn't it be better to have one standard mapping between color palettes made by trusted Apple Designers than everyone trying to interpolate from the standard colors, or just guessing the best color?

# A proposition
One option for translating a color from one palette to another, would be giving each instance of UIColor a property that stores current variant and a method to(variant: Variant), with Variant being an enum of possible color palettes. Now there are two such contexts, corresponding to light and dark mode, but theoretically could be many more. 

# TO DO: 
code
