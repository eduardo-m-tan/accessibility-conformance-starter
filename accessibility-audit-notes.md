# Accessibility Audit Notes

## Automated Check Used: axe DevTools v4.138.0
- Findings:
    - Buttons without discernable text are present, issue for screen readers
    - "More" buttons in the sessions cards do not meet WCAG 2 AA minimum contrast ratio thresholds, issue for low vision users
    - Tool does not identify labels in the form since they are not attached in the native HTML, issue for screen readers
    - Improper heading order usage, issue for screen readers
- These all impact accessibility usage in a couple of areas but primarily for screen reader users. 

## Keyboard navigation and focus-visible:
- Utilized the web accessibility evaluation (WAVE) tool to complete this test since no focus-visible pseudo class is used
- Keyboard navigation follows logical order of nav then top to bottom for other links/buttons/forms
- No focus-visible pseudo class is used, creates a difficult time using keyboard navigation, must be fixed for those with limited movement usage on a webpage.

## Landmarks. headings, links, buttons, image alt check: 
- Landmarks are discernable, navigation is located in the header
- Main area is clear and flows normally aside from one heading out of place in the 'Community Tech Day' box, issue for scanning and assistive-tech navigation
- Links stating 'more' could be more specific, WAVE tool gives a warning saying the links may not make sense out of context
- As the axe DevTools found, there is a button without discernable text present
- Alt descriptions are available but vary in how descriptive they are (despite being the same session poster image), should align in terms of how appropriate it is

## Zoom and reflow check (200%), narrow responsive check: 
- Zoom test completed in Chrome at 200%, page has a horizontal scrollbar and doesn't resize itself appropriately, although most content is still viewable
- Narrow viewport tested in Chrome DevTools at narrow responsive width, not all content is easily accessible and requires horizontal scrolling, main content is not easily readable

### Five issues and three documented fixes:
- Form has issues like a button missing text and missing or unlinked labels
    - Form labels were linked and button text was added
- No focus-visible was used so keyboard navigation is difficult to utilize
    - Two-layered focus-visible outline was added with two colors, allows for contrast on any background that is present in this document
- 'More' buttons could use improved text like "Learn More" and need to have better color contrast to background
    - Color of links were changed to the maroon color of the rest of the page to contrast more properly, "Learn More" was substituted in for a better description
- Heading order in the first section was used improperly, breaks flow
- Zoom and resizing flow needs to be fixed, horizontal scrolling is bad usability for all users

### Retesting notes:
- 