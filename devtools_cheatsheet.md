# Chrome DevTools Cheatsheet

## Opening DevTools
- **F12** or **Ctrl+Shift+I** (Windows/Linux)
- **Cmd+Option+I** (Mac)
- **Right-click → Inspect**
- **Ctrl+Shift+C** (Element picker mode)

## Main Panels Overview

### Elements Panel
**Purpose**: Inspect and modify HTML/CSS in real-time

#### Key Features
- **Select Element**: Click the cursor icon or press **Ctrl+Shift+C**
- **Edit HTML**: Double-click any element to edit
- **CSS Editing**: 
  - Click any CSS property to edit
  - Add new properties by clicking empty space
  - Toggle properties with checkbox
- **Computed Styles**: See final applied styles
- **Box Model**: Visualize padding, border, margin

#### Quick Actions
- **H** - Hide element
- **Delete** - Remove element
- **F2** - Edit as HTML

### Console Panel
**Purpose**: JavaScript execution, debugging, and logging

#### Essential Commands
```javascript
// Basic logging
console.log("Hello World");
console.error("Error message");
console.warn("Warning message");

// Inspect elements
$0 // Last selected element
$1 // Second-to-last selected element
$() // Same as document.querySelector()
$$() // Same as document.querySelectorAll()

// Clear console
clear()

// Measure performance
console.time("myTimer");
// ... code to measure
console.timeEnd("myTimer");
```

### Network Panel
**Purpose**: Monitor all network requests and responses

#### Key Information
- **Status Codes**: 200 (OK), 404 (Not Found), 500 (Server Error)
- **Method**: GET, POST, PUT, DELETE
- **Size**: Actual vs. transferred size
- **Time**: Request duration
- **Waterfall**: Visual timeline of requests

#### Useful Features
- **Filter by type**: JS, CSS, Images, XHR, etc.
- **Throttling**: Simulate slow connections
- **Block requests**: Right-click → Block request URL
- **Export HAR**: Save network data for analysis

### Sources Panel
**Purpose**: Debug JavaScript code

#### Debugging Features
- **Breakpoints**: Click line number to set
- **Conditional Breakpoints**: Right-click line number
- **Watch Expressions**: Monitor variable values
- **Call Stack**: See function execution path
- **Scope**: View local and global variables

#### Keyboard Shortcuts
- **F8** - Resume execution
- **F10** - Step over
- **F11** - Step into
- **Shift+F11** - Step out

### Performance Panel
**Purpose**: Analyze runtime performance and identify bottlenecks

#### Key Metrics
- **FPS**: Frames per second
- **CPU Usage**: Processing time breakdown
- **Network**: Request timing
- **Screenshots**: Visual progression

### Application Panel
**Purpose**: Inspect stored data and PWA features

#### Storage Types
- **Local Storage**: Persistent key-value storage
- **Session Storage**: Temporary key-value storage
- **Cookies**: HTTP cookies with expiration
- **IndexedDB**: Large-scale data storage
- **Service Workers**: Background scripts

### Security Panel
**Purpose**: Check HTTPS and certificate information

#### Security Indicators
- **Secure**: Valid HTTPS with trusted certificate
- **Info**: Mixed content warnings
- **Not Secure**: HTTP or certificate issues

## Device Testing

### Responsive Design Mode
- **Ctrl+Shift+M** (Windows/Linux)
- **Cmd+Shift+M** (Mac)

#### Features
- **Device Presets**: iPhone, iPad, Android devices
- **Custom Dimensions**: Set specific width/height
- **Orientation**: Portrait/Landscape toggle
- **Zoom Levels**: 25% to 500%
- **Touch Simulation**: Enable touch events

## Performance Tips

### For Developers
- Use **Lighthouse** tab for performance audits
- Monitor **Memory** tab for memory leaks
- Check **Coverage** tab for unused CSS/JS
- Use **Rendering** tab to identify paint issues

### For Marketing/SEO
- **Network** panel: Check page load times
- **Lighthouse**: Get SEO and accessibility scores
- **Application** panel: Verify tracking pixels
- **Security** panel: Ensure HTTPS compliance

### For InfoSec
- **Network** panel: Monitor all requests
- **Application** panel: Inspect stored data
- **Security** panel: Check certificate validity
- **Console** panel: Look for security warnings

## Quick Shortcuts Summary

| Action | Windows/Linux | Mac |
|--------|---------------|-----|
| Open DevTools | F12 | Cmd+Option+I |
| Element Picker | Ctrl+Shift+C | Cmd+Shift+C |
| Console | Ctrl+Shift+J | Cmd+Option+J |
| Responsive Mode | Ctrl+Shift+M | Cmd+Shift+M |
| Hard Refresh | Ctrl+Shift+R | Cmd+Shift+R |
| Screenshot | Ctrl+Shift+P → "screenshot" | Cmd+Shift+P → "screenshot" |

## Common Use Cases

### Web Development
- Debug JavaScript errors
- Test responsive layouts
- Optimize loading performance
- Validate HTML/CSS

### Marketing Analysis
- Check tracking code implementation
- Analyze page load speeds
- Test mobile experience
- Verify A/B test configurations

### Security Testing
- Inspect network traffic
- Check for mixed content
- Validate SSL certificates
- Monitor data storage practices

## Pro Tips
1. **Command Menu**: Press **Ctrl+Shift+P** (Cmd+Shift+P on Mac) to access all DevTools features
2. **Dark Theme**: Settings → Preferences → Theme → Dark
3. **Dock Position**: Click the three dots → Dock side (bottom, right, separate window)
4. **Device Mode Screenshots**: Capture full page or visible area screenshots
5. **Network Throttling**: Test slow connections without changing your internet
6. **Local Overrides**: Replace remote files with local versions for testing