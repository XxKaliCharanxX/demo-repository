# Setting Up Labels and Starter Issues

## 🏷️ Step 1: Create Labels

Run these commands to create all labels:

```bash
# Difficulty
gh label create "good first issue" -d "Perfect for first-time contributors" -c "7057ff"
gh label create "beginner friendly" -d "Easy tasks, no coding experience required" -c "00d084"
gh label create "intermediate" -d "Requires some coding knowledge" -c "ffa500"
gh label create "advanced" -d "Complex task requiring experience" -c "ff0000"

# Type
gh label create "bug" -d "Something isn't working" -c "d73a4a"
gh label create "enhancement" -d "New feature or request" -c "a2eeef"
gh label create "documentation" -d "Improvements or additions to documentation" -c "0075ca"
gh label create "content" -d "Update text, images, or content" -c "1d76db"

# Area
gh label create "html" -d "HTML structure changes" -c "e99695"
gh label create "css" -d "Styling and design" -c "c5def5"
gh label create "javascript" -d "JavaScript functionality" -c "f9d0c4"
gh label create "design" -d "UI/UX design improvements" -c "d4c5f9"

# Community
gh label create "help wanted" -d "Extra attention is needed" -c "fbca04"
gh label create "question" -d "Further information is requested" -c "d876e3"
gh label create "discussion" -d "Discussion needed before implementation" -c "cc317c"

# Priority
gh label create "priority: low" -d "Low priority" -c "c2e0c6"
gh label create "priority: medium" -d "Medium priority" -c "fbca04"
gh label create "priority: high" -d "High priority" -c "ff6b6b"

# Status
gh label create "blocked" -d "Blocked by other issues or dependencies" -c "b60205"
gh label create "in progress" -d "Someone is actively working on this" -c "0e8a16"
gh label create "needs review" -d "Ready for review" -c "fbca04"

# Special
gh label create "hacktoberfest" -d "Eligible for Hacktoberfest" -c "ff6b6b"
```

## 📝 Step 2: Create Starter Issues

Copy and paste these issue templates into GitHub:

---

### Issue 1: Update Footer Copyright Year

**Title:** Update footer copyright year to 2025

**Labels:** `good first issue`, `beginner friendly`, `content`, `html`

**Description:**

````markdown
## Description

The footer currently shows "© 2025" but we should make it dynamic or at least update it regularly.

## Task

Update the copyright year in the footer section of `index.html`.

**Location:** `index.html` line ~657

**Current:**

```html
<p>© 2025 Mauritania Programmers Community. All rights reserved.</p>
```
````

**Change to:**

```html
<p>© 2025 Mauritania Programmers Community. All rights reserved.</p>
```

## Skills Needed

- Basic HTML knowledge
- Text editing

## Steps

1. Fork the repository
2. Edit `index.html`
3. Find the footer section
4. Update the year
5. Commit and create a PR

## Resources

- [HTML Basics](https://developer.mozilla.org/en-US/docs/Learn/HTML)
- [Contributing Guide](CONTRIBUTING.md)

Need help? Ask in the comments!

````

---

### Issue 2: Add Alt Text to Images

**Title:** Add descriptive alt text to all images for accessibility

**Labels:** `good first issue`, `beginner friendly`, `html`, `accessibility`

**Description:**
```markdown
## Description
Some images are missing descriptive alt text, which is important for:
- Screen reader users
- SEO
- When images fail to load

## Task
Add meaningful alt text to images in `index.html`.

**Example:**
```html
<!-- Current -->
<img src="./assets/images/MPC.png" alt="MPC Logo">

<!-- Could be more descriptive -->
<img src="./assets/images/MPC.png" alt="Mauritania Programmers Community Logo - Green crescent and gold star">
````

## Images to Update

- Logo in header
- Any project screenshots (if added)
- Event images (if added)

## Skills Needed

- Basic HTML
- Understanding of accessibility

## Resources

- [Alt Text Best Practices](https://www.w3.org/WAI/tutorials/images/)
- [WCAG Guidelines](https://www.w3.org/WAI/WCAG21/Understanding/non-text-content.html)

````

---

### Issue 3: Add Mobile Menu (Hamburger)

**Title:** Implement mobile hamburger menu navigation

**Labels:** `enhancement`, `intermediate`, `javascript`, `html`, `css`

**Description:**
```markdown
## Description
Currently, the navigation shows all links on desktop but they might overflow on mobile. We need a hamburger menu for small screens.

## Task
1. Add hamburger icon (☰) that shows on mobile (<768px)
2. Hide regular navigation on mobile
3. Toggle menu visibility when hamburger is clicked
4. Add smooth animation

## Files to Modify
- `index.html` - Add hamburger button
- `css/custom.css` - Add mobile styles
- `js/app.js` - Add toggle functionality (placeholder already exists!)

## Reference
There's already a placeholder function in `js/app.js:171`:
```javascript
function initMobileMenu() {
  // This is a placeholder for future mobile menu functionality
  console.log('Mobile menu functionality ready for implementation');
}
````

## Skills Needed

- HTML
- CSS (media queries)
- JavaScript (DOM manipulation)

## Resources

- [Responsive Navigation](https://www.w3schools.com/howto/howto_js_mobile_navbar.asp)
- [CSS Media Queries](https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries)

````

---

### Issue 4: Add Dark Mode Toggle

**Title:** Implement dark mode theme toggle

**Labels:** `enhancement`, `intermediate`, `javascript`, `css`, `design`

**Description:**
```markdown
## Description
Add a dark mode option for better accessibility and user preference.

## Task
1. Add dark mode toggle button in header
2. Create CSS variables for colors
3. Implement dark theme styles
4. Save preference to localStorage
5. Respect system preference (prefers-color-scheme)

## Implementation Ideas
```javascript
// Detect system preference
const darkModePreference = window.matchMedia('(prefers-color-scheme: dark)');

// Save to localStorage
localStorage.setItem('theme', 'dark');
````

```css
/* CSS Variables */
:root {
  --bg-color: white;
  --text-color: #0a1628;
}

[data-theme="dark"] {
  --bg-color: #0a1628;
  --text-color: white;
}
```

## Skills Needed

- JavaScript
- CSS (custom properties)
- localStorage API

## Resources

- [Dark Mode Guide](https://css-tricks.com/a-complete-guide-to-dark-mode-on-the-web/)

````

---

### Issue 5: Improve README with Setup GIF

**Title:** Add visual setup guide with animated GIF/screenshot

**Labels:** `good first issue`, `documentation`, `content`

**Description:**
```markdown
## Description
A picture is worth a thousand words! Add screenshots or an animated GIF showing how to:
- Clone the repository
- Open index.html
- See the result

## Task
1. Create screenshots or record GIF of setup process
2. Add to `README.md`
3. Store images in `assets/screenshots/` folder

## Tools for GIFs
- [ScreenToGif](https://www.screentogif.com/) (Windows)
- [Kap](https://getkap.co/) (Mac)
- [Peek](https://github.com/phw/peek) (Linux)

## Skills Needed
- Basic Markdown
- Screen recording
- File organization

## Resources
- [Markdown Images](https://www.markdownguide.org/basic-syntax/#images-1)
````

---

### Issue 6: Add "Back to Top" Button

**Title:** Add smooth scroll to top button

**Labels:** `enhancement`, `beginner friendly`, `javascript`, `css`

**Description:**

````markdown
## Description

When users scroll down, show a "Back to Top" button that smoothly scrolls to the top of the page.

## Task

1. Add button HTML (hidden by default)
2. Show button when user scrolls down >300px
3. Add click handler to scroll to top smoothly
4. Style with MPC brand colors

## Example Implementation

```javascript
// Show/hide based on scroll
window.addEventListener("scroll", () => {
  const scrollTop = document.querySelector(".scroll-to-top");
  if (window.pageYOffset > 300) {
    scrollTop.classList.add("visible");
  } else {
    scrollTop.classList.remove("visible");
  }
});
```
````

## Skills Needed

- HTML
- CSS (positioning, transitions)
- JavaScript (event listeners)

## Resources

- [Scroll Events](https://developer.mozilla.org/en-US/docs/Web/API/Document/scroll_event)
- [Smooth Scroll](https://developer.mozilla.org/en-US/docs/Web/API/Window/scrollTo)

````

---

### Issue 7: Add Loading Animation

**Title:** Add page loading animation/spinner

**Labels:** `enhancement`, `beginner friendly`, `css`, `design`

**Description:**
```markdown
## Description
Add a simple loading animation that shows while the page loads.

## Task
1. Create CSS spinner animation
2. Show on page load
3. Hide when page fully loaded
4. Use MPC brand colors (green & gold)

## Reference
There's already a spinner animation in `css/custom.css:225`!

## Skills Needed
- CSS (animations, keyframes)
- Basic JavaScript (DOMContentLoaded)

## Resources
- [CSS Animations](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Animations)
- [Loading Spinners](https://loading.io/css/)
````

---

## 🎯 How to Use These Issues

1. **Copy the issue content** from above
2. **Go to your repository** → Issues → New Issue
3. **Paste the content**
4. **Add the labels** mentioned for each issue
5. **Create the issue**

## 📊 Label Best Practices

### For Beginners:

- Always tag with `good first issue` or `beginner friendly`
- Provide clear, step-by-step instructions
- Link to resources and documentation
- Offer help in comments

### For Organization:

- Use multiple labels (difficulty + type + area)
- Update labels as issue progresses
- Use `in progress` when someone is working on it
- Close with reference to PR

## 🚀 Bonus: Hacktoberfest

If you participate in Hacktoberfest, add the `hacktoberfest` label to eligible issues!
