# Chrome DevTools Workshop: Hands-On Troubleshooting Guide

## Workshop Overview (5 minutes)
**Goal**: Give team members practical skills to troubleshoot web applications using Chrome DevTools

**What We'll Cover**:
- Opening DevTools (multiple ways)
- Console fundamentals for debugging
- Essential tabs: Elements, Network, Application
- Real troubleshooting scenarios you can practice

---

## Part 1: Getting Started with DevTools (10 minutes)

### Opening DevTools - Try All These Methods!

**Method 1: Right-click Menu**
1. Go to any website (try `example.com`)
2. Right-click anywhere on the page
3. Select "Inspect" or "Inspect Element"

**Method 2: Keyboard Shortcuts** ⭐ *Most Important*
- **Windows/Linux**: `Ctrl + Shift + I` (Inspector) or `Ctrl + Shift + J` (Console)
- **Mac**: `Cmd + Option + I` (Inspector) or `Cmd + Option + J` (Console)

**Method 3: Chrome Menu**
- Click the three dots (⋮) in Chrome
- More Tools → Developer Tools

### Quick DevTools Tour
- **Docking Options**: Try undocking DevTools (click the ⋮ in DevTools)
- **Main Tabs**: Elements, Console, Sources, Network, Performance, Memory, Application

---

## Part 2: Console Fundamentals (15 minutes)

### Exercise 1: Basic Console Commands
Open the Console tab and try these commands:

```javascript
// Basic output
console.log("Hello, DevTools!");

// Check what page you're on
window.location.href

// See all available console methods
console

// Clear the console
clear()
```

### Exercise 2: Inspecting Page Elements
```javascript
// Get the page title
document.title

 

// Count how many links are on the page
document.querySelectorAll('a').length

// Change the page title (temporarily)
document.title = "I changed this with DevTools!"
```

### Exercise 3: Console Utility Functions
```javascript
// Select elements (like jQuery $)
$('h1')  // First h1 element
$$('p')  // All paragraph elements

// Inspect an element in detail
inspect($('h1'))

// Copy something to clipboard
copy(document.title)
```

### Exercise 4: Debugging with Console
```javascript
// Time how long something takes
console.time('page-load-check');
// ... do something ...
console.timeEnd('page-load-check');

// Create a table from data
console.table([
  {name: 'Chrome', version: '122'},
  {name: 'Firefox', version: '123'},
  {name: 'Safari', version: '17'}
]);

// Group related logs
console.group('User Data');
console.log('Name: John');
console.log('Email: john@example.com');
console.groupEnd();
```

---

## Part 3: Elements Tab - Live Editing (10 minutes)

### Exercise 5: Inspect and Edit HTML
1. Go to `https://example.com`
2. Right-click on the main heading and select "Inspect"
3. **Double-click** the text in the Elements panel
4. Change it to "I edited this live!"
5. Press Enter to apply

### Exercise 6: Edit CSS Styles
1. With an element selected, look at the Styles panel
2. Click in the `element.style {}` section
3. Add: `color: red; font-size: 30px;`
4. Watch the page change in real-time!

### Exercise 7: Find Elements Fast
1. Press `Ctrl+F` (or `Cmd+F`) while in Elements tab
2. Search for: `<img`
3. See all images highlighted
4. Try searching for CSS classes: `.container`

---

## Part 4: Network Tab - Understanding Traffic (15 minutes)

### Exercise 8: Monitor Network Requests
1. Open the Network tab
2. **Refresh the page** (`F5` or `Ctrl+R`)
3. Watch all the files load!
4. Click on any request to see details

### Exercise 9: Filter Network Traffic
Try these filters in the Network tab:
- Click **XHR** to see only API calls
- Click **Img** to see only images
- Click **JS** to see only JavaScript files
- Use the search box to find specific files

### Exercise 10: Simulate Slow Connections
1. In Network tab, find the "Throttling" dropdown (might say "No throttling")
2. Select "Slow 3G"
3. Refresh the page
4. See how slow it loads!
5. **Don't forget to change it back to "No throttling"**

### Exercise 11: Check for Errors
1. Look for red entries in the Network tab (failed requests)
2. Click on any red entry to see why it failed
3. Check the Status column for error codes (404, 500, etc.)

---

## Part 5: Application Tab - Stored Data (10 minutes)

### Exercise 12: Explore Stored Data
1. Go to a site you use regularly (like Gmail, Facebook, or GitHub)
2. Open the Application tab
3. Expand "Local Storage" in the left sidebar
4. Click on the domain name
5. See what data the site stores about you!

### Exercise 13: Manage Cookies
1. In Application tab, expand "Cookies"
2. Click on the domain
3. See all cookies stored
4. Try deleting a cookie (right-click → Delete)

### Exercise 14: Check Storage Usage
1. In Application tab, click on "Storage" in the left sidebar
2. See how much space the website is using
3. You can clear storage for testing

---

## Part 6: Real Troubleshooting Scenarios (15 minutes)

### Scenario 1: "The page won't load"
**Steps to investigate:**
1. Open Network tab
2. Refresh page
3. Look for red (failed) requests
4. Check Console for JavaScript errors
5. Look for 404s, 500s, or timeout errors

### Scenario 2: "The page is really slow"
**Steps to investigate:**
1. Network tab → Check file sizes (Size column)
2. Look for large images or JS files
3. Use Throttling to test on slow connections
4. Console → Run: `console.time('test'); location.reload();`

### Scenario 3: "My changes aren't showing up"
**Steps to investigate:**
1. Console → Type: `location.reload(true)` (hard refresh)
2. Network tab → Check "Disable cache" checkbox
3. Application tab → Clear storage if needed
4. Check if files are actually loading (Network tab)

### Scenario 4: "Something's broken but I don't know what"
**Steps to investigate:**
1. Console tab → Look for red error messages
2. Elements tab → Check if HTML looks correct
3. Network tab → Look for failed requests
4. Application tab → Check if required data is stored

---

## Part 7: Essential DevTools Tips (5 minutes)

### Pro Tips for Daily Use

**Console Shortcuts:**
- `↑` and `↓` arrows: Navigate command history
- `Ctrl+L` or `Cmd+K`: Clear console
- `Shift+Enter`: New line without executing

**General Tips:**
- **Preserve log**: Check this in Console/Network to keep logs during page navigation
- **Disable cache**: Check this in Network tab when testing changes
- **Device simulation**: Click the device icon to test mobile views

### Quick Reference Card
```
Open DevTools:     Ctrl+Shift+I (Windows) / Cmd+Option+I (Mac)
Open Console:      Ctrl+Shift+J (Windows) / Cmd+Option+J (Mac)
Inspect Element:   Right-click → Inspect
Clear Console:     Ctrl+L or clear()
Search Elements:   Ctrl+F in Elements tab
Hard Refresh:      Ctrl+Shift+R (clears cache)
```

---

## Hands-On Practice: Try These Now!

### Practice Exercise 1: Debug a Broken Page
1. Go to: `https://httpstat.us/500`
2. Open DevTools
3. Find the error in Network tab
4. What status code do you see?

### Practice Exercise 2: Edit a Live Site
1. Go to any news website
2. Use Elements tab to change a headline
3. Use Console to count how many articles are on the page:
   ```javascript
   document.querySelectorAll('article').length
   ```

### Practice Exercise 3: Check Storage
1. Go to your favorite social media site
2. Application tab → Local Storage
3. How much data do they store about you?
4. Application tab → Cookies
5. How many cookies do they have?

---

## Troubleshooting Cheat Sheet

| Problem | Where to Look | What to Check |
|---------|---------------|---------------|
| Page won't load | Network tab | Failed requests (red), 404/500 errors |
| JavaScript errors | Console tab | Red error messages |
| Styling issues | Elements tab | CSS styles, computed values |
| Slow loading | Network tab | File sizes, waterfall timing |
| Data not saving | Application tab | Local Storage, Cookies |
| Cache issues | Network tab | Disable cache checkbox |

---

## Next Steps

**For Further Learning:**
1. **Performance tab**: Analyze page speed in detail
2. **Sources tab**: Debug JavaScript with breakpoints
3. **Security tab**: Check HTTPS and certificate issues
4. **Lighthouse**: Automated audits for performance, SEO, accessibility

**Practice Regularly:**
- Use DevTools every time you browse
- Practice on different websites
- Try breaking things intentionally to learn how to fix them

**Advanced Topics for Later:**
- Mobile device simulation
- Network throttling for testing
- JavaScript debugging with breakpoints
- Performance profiling
