# Chrome DevTools Workshop - Complete Teaching Script

## Pre-Workshop Setup (5 minutes before start)
- Ensure all participants have Chrome browser installed (latest version)
- Test screen sharing/projection setup
- Have sample websites ready:
  - https://example.com (for basic exercises)
  - https://httpbin.org (for network testing)
  - A simple HTML page with intentional issues (create locally)
- Distribute cheatsheet handouts

---

## Hour 1: Foundation & Setup (60 minutes)

### Opening & Introductions (10 minutes)

**[Start with energy and enthusiasm]**

"Good morning everyone! Welcome to our Chrome DevTools workshop. Before we dive in, let's do quick introductions. I'd like each of you to share:
- Your name
- Your role (developer, marketing, security, etc.)
- One thing you hope to accomplish with DevTools today

**[Go around the room, take notes of roles for later reference]**

Great! I can see we have a fantastic mix of backgrounds here. That's exactly what makes DevTools so powerful - it's one tool that serves multiple disciplines.

**Course Objectives - What You'll Walk Away With:**
- Confidence using DevTools for your specific role
- Practical skills you can apply immediately
- Understanding of how DevTools can improve your daily workflow
- A cheatsheet you can reference later

**Why This Matters:**
- **Developers**: Debug faster, optimize better
- **Marketing**: Verify campaigns, improve conversion rates
- **InfoSec**: Identify vulnerabilities, monitor traffic
- **Everyone**: Understand how websites really work

Let's get started!

### DevTools Fundamentals (20 minutes)

**[Open Chrome to google.com]**

"First question - how many of you have accidentally opened DevTools before and immediately closed it because it looked intimidating?"

**[Pause for responses, acknowledge the common experience]**

"Perfect - that's exactly why we're here. DevTools looks complex, but it's just organized tools for understanding websites.

#### What Are Chrome DevTools?

Think of DevTools as a Swiss Army knife for websites. Just like a Swiss Army knife has different tools for different jobs, DevTools has different panels for different tasks.

**[Demonstrate opening DevTools multiple ways]**

Let me show you the three main ways to open DevTools:

1. **Right-click anywhere on a webpage → Inspect**
   - This is intuitive - you're saying 'I want to inspect this'
   
2. **Press F12** (or Ctrl+Shift+I on Windows, Cmd+Option+I on Mac)
   - This is the fastest once you memorize it
   
3. **Chrome Menu → More Tools → Developer Tools**
   - This is the 'official' way, but slowest

**[Open DevTools using F12]**

#### Interface Overview

**[Point to each area as you describe it]**

Look at what we have here:
- **Top bar with tabs**: These are our different 'tools' - Elements, Console, Sources, etc.
- **Main panel**: This shows the content for whichever tab is selected
- **Left side**: Usually shows the structure (like HTML)
- **Right side**: Usually shows details or properties

**Important**: Don't try to understand everything at once. We'll explore each panel step by step.

#### Customizing Your Workspace

**[Demonstrate each docking option]**

DevTools can be positioned three ways:
1. **Bottom dock** (default) - Good for wide screens
2. **Right dock** - Better for tall content
3. **Separate window** - Great for dual monitors

**[Click the three dots menu → Dock side, show each option]**

Try different positions and see what feels comfortable. There's no 'right' way - it's personal preference.

**[Go to Settings (gear icon)]**

Quick settings tour:
- **Theme**: Light vs Dark (I prefer dark, easier on the eyes)
- **Panel layout**: Can be customized
- **Shortcuts**: All the keyboard shortcuts

**Your Turn - 2 Minutes:**
- Open DevTools on any website
- Try different dock positions
- Switch to dark theme if you like
- Click through the main tabs just to see them

**[Wait 2 minutes, walk around and help]**

### Elements Panel Deep Dive (25 minutes)

**[Navigate to a simple website like example.com]**

"The Elements panel is where most people start, and for good reason - it shows you the 'skeleton' of any webpage.

#### Understanding What You're Looking At

**[Point to the left side of Elements panel]**

This left side shows the HTML - the structure of the page. Think of HTML like the frame of a house - it defines where everything goes.

**[Point to the right side]**

This right side shows the CSS - the styling. Think of CSS like the paint, wallpaper, and decorations of the house.

#### Element Selection - Your New Superpower

**[Click the element selector icon]**

This cursor icon is magic. When you click it, you can hover over ANY part of a webpage and see exactly how it's built.

**[Hover over different elements, point out the highlighting]**

See how it highlights different parts? The blue is the content, green is padding, yellow is margin. Don't worry about remembering these colors - just know that different parts are highlighted differently.

**[Click on a heading element]**

When I click, notice two things:
1. The HTML on the left shows exactly where this element is
2. The CSS on the right shows all the styling rules

#### Live HTML Editing

**[Double-click on text in the HTML panel]**

Here's something cool - I can edit this directly.

**[Change text content]**

Watch the webpage change in real-time! This only changes your local view - I'm not hacking the website. It's like using White-Out on a newspaper - only you see the changes.

**Practical Uses:**
- **Marketing**: Test different headline copy instantly
- **Developers**: Try fixes before writing code
- **InfoSec**: See if you can inject content (in a safe environment)

#### CSS Magic

**[Click on an element with visible styling]**

Now for the really fun part - CSS editing.

**[In the Styles panel on the right, click on a color value]**

When I click on this color, I get a color picker. I can change any color instantly.

**[Change the color, show the effect]**

**[Click on a font-size value]**

I can change sizes, fonts, anything. Use the up/down arrows or just type new values.

**[Show adding a new CSS property]**

To add completely new styling, click in the empty space here and type. Let me add a border...

**[Type: border: 5px solid red]**

Instant red border! 

#### Box Model Visualization

**[Scroll down to the Computed section or Box Model diagram]**

This diagram shows you exactly how much space each element takes up:
- **Blue center**: The actual content
- **Green**: Padding (space inside the element)
- **Yellow**: Margin (space outside the element)
- **Orange**: Border

**[Hover over different parts of the box model]**

Watch how hovering here highlights the actual webpage - this helps you understand spacing issues.

#### Hands-on Exercise (8 minutes)

**Your Mission:**
1. Go to any news website (CNN, BBC, your choice)
2. Use element selector to click on a headline
3. Change the headline text to something funny
4. Change the text color to red
5. Add a yellow background (background-color: yellow)
6. Take a screenshot to show your neighbor

**Bonus Points:**
- Hide an entire section (right-click element → Hide element)
- Change a font size to be huge (font-size: 50px)

**[Walk around helping participants, encourage experimentation]**

**[After 8 minutes, call attention back]**

"Who found something interesting or fun? Let's see a few examples!"

**[Have 2-3 people share their screens briefly]**

### Q&A and Break (5 minutes)

"Quick questions before we move on to some really powerful stuff:
- Any confusion about what we've covered?
- Anyone having trouble with the basics?
- Ready to see how this applies to your specific work?"

**[Take a 5-minute break]**

---

## Hour 2: Core Panels & Practical Applications (60 minutes)

### Console Panel & JavaScript Basics (20 minutes)

**[Switch to Console tab]**

"Welcome back! The Console is where websites 'talk' to you. Every error, every debug message, every warning shows up here.

#### Why the Console Matters for Everyone

**[Type in console: console.log('Hello everyone!')]**

Even if you're not a programmer, the console gives you insights:
- **Marketing**: Are tracking scripts working?
- **InfoSec**: Are there security warnings?
- **Developers**: What errors need fixing?

#### Reading Console Messages

**[Navigate to a website with some console activity]**

Let's look at what we see here:
- **Red messages**: Errors - something is broken
- **Yellow messages**: Warnings - something might be wrong
- **Blue/white messages**: Info - just notifications

**[Point to different types of messages]**

Don't panic if you see red! Not all errors break the site. Think of them like 'check engine' lights - some are urgent, some aren't.

#### Useful Console Commands for Non-Programmers

**[Type each command and explain]**

```javascript
// This shows you the last element you clicked
$0
```

**[Click an element first, then type $0]**

See? It references that exact element.

```javascript
// This clears all the messy output
clear()
```

**[Execute clear()]**

Much cleaner!

```javascript
// This finds elements on the page
$('h1')
```

**[Execute the command]**

This finds the first headline on the page. Think of it like Ctrl+F but more powerful.

#### Role-Specific Console Applications

**For Marketing Teams:**

**[Navigate to a site with Google Analytics]**

```javascript
// Check if Google Analytics is loaded
ga
```

If this shows a function, GA is working. If it shows 'undefined', there's a problem.

**[Type: dataLayer]**

This shows if Google Tag Manager data is flowing correctly.

**For InfoSec Teams:**

**[Show security warnings in console]**

Security warnings often appear here first:
- Mixed content warnings (HTTP content on HTTPS sites)
- Blocked scripts from unsafe sources
- Cookie security issues

**For Developers:**

**[Show error stack traces]**

Errors show you exactly where problems occur, with line numbers and file names.

#### Hands-on Exercise (5 minutes)

**Everyone try these:**
1. Type `console.log('Your name is awesome!')` and press Enter
2. Type `clear()` to clean up
3. Click on any element on the page, then type `$0` to see it referenced
4. Look for any red error messages - don't fix them, just observe

**Advanced (if comfortable):**
- Type `document.title` to see the page title
- Type `location.href` to see the current URL

### Network Panel & Performance Monitoring (25 minutes)

**[Switch to Network tab]**

"The Network panel shows you EVERYTHING that loads when you visit a webpage. This is incredibly powerful for all our roles.

#### Understanding the Network Panel

**[Refresh the page to populate network requests]**

Look at this waterfall chart. Each bar represents something being downloaded:
- Images
- CSS files
- JavaScript files
- Data from APIs
- Tracking pixels

**[Point to different elements]**

#### Reading the Network Information

**[Click on a request to show details]**

For each request, we can see:
- **Status**: 200 is good, 404 means missing, 500 means server error
- **Size**: How big the file is
- **Time**: How long it took to download
- **Type**: What kind of file it is

#### Marketing Applications

**[Look for tracking pixels or analytics requests]**

**For Marketing Teams, this panel is gold:**
- Verify Google Analytics is firing
- Check if Facebook Pixel is working
- See how fast your landing pages load
- Identify what's slowing down conversions

**[Point to GA requests]**

See these requests to google-analytics.com? That means your tracking is working.

**[Point to large images]**

See this 2MB image? That's probably slowing down your mobile users.

#### Security Applications

**[Filter by different request types]**

**For InfoSec Teams:**
- Monitor all API calls and data transfers
- Identify unsecured HTTP requests on HTTPS sites
- See what third-party services have access to your data
- Check for unusual or suspicious requests

**[Right-click on a request → Copy → Copy as cURL]**

You can even recreate any request for testing purposes.

#### Performance Analysis

**[Show the timeline view]**

This timeline shows the loading sequence:
- **Blue line**: DOM content loaded (page structure ready)
- **Red line**: Page fully loaded (everything including images)

**[Point to slow requests]**

Anything taking more than 2-3 seconds on a good connection is a problem for user experience.

#### Network Panel Features

**[Demonstrate each feature]**

**Filtering:**
- Click 'JS' to see only JavaScript files
- Click 'XHR' to see data requests
- Click 'Img' to see only images

**Throttling:**
**[Click the throttling dropdown]**

This simulates slow connections:
- 'Slow 3G' shows you mobile user experience
- 'Fast 3G' shows you average mobile experience

**[Enable slow 3G and refresh page]**

Now you see what your mobile users experience!

**Blocking Requests:**
**[Right-click on a request → Block request URL]**

This lets you test what happens if certain resources fail to load.

#### Hands-on Exercise (12 minutes)

**Choose Your Adventure Based on Your Role:**

**Marketing Focus:**
1. Go to your company website (or any e-commerce site)
2. Open Network panel and refresh
3. Look for Google Analytics requests (google-analytics.com)
4. Check total page load time (bottom status bar)
5. Enable 'Slow 3G' throttling and refresh - how long does it take?
6. Find the largest image - could it be optimized?

**InfoSec Focus:**
1. Go to a major website (bank, news site)
2. Check for any HTTP requests on an HTTPS site (security issue)
3. Look at the third-party domains being contacted
4. Check for any failed requests (red status codes)
5. Export the data (right-click → Save as HAR file)

**Developer Focus:**
1. Find a website with performance issues
2. Identify the slowest-loading resources
3. Check for 404 errors (missing files)
4. Use throttling to test different connection speeds
5. Try blocking a non-critical resource to see the impact

**[Walk around helping different groups, answer specific questions]**

### Device Testing & Responsive Design (15 minutes)

**[Press Ctrl+Shift+M to enter device mode]**

"Mobile traffic now exceeds desktop traffic for most websites. The device testing features in DevTools are essential for everyone.

#### Responsive Design Mode

**[Show the device toolbar]**

This toolbar gives you superpowers:
- Test different screen sizes instantly
- Simulate touch interactions
- Check how your site looks on specific devices

#### Device Presets

**[Click through different device presets]**

DevTools includes presets for popular devices:
- iPhone 14, iPhone SE (for mobile testing)
- iPad (for tablet testing)
- Various Android devices

**[Show landscape/portrait toggle]**

Don't forget to test both orientations!

#### Custom Dimensions

**[Show custom size controls]**

You can also set exact dimensions:
- 1920x1080 for desktop
- 768px width for typical tablet breakpoint
- 320px width for small mobile

#### Touch Simulation

**[Enable touch simulation in settings]**

When enabled, this changes mouse interactions to touch interactions, helping you test mobile user experience more accurately.

#### Real-World Applications

**For Marketing:**
- Test your checkout flow on mobile
- Verify your CTA buttons are finger-friendly
- Check that your forms work on small screens

**For Developers:**
- Debug responsive CSS breakpoints
- Test navigation on different screen sizes
- Verify touch interactions

**For InfoSec:**
- Ensure security warnings display properly on mobile
- Test 2FA flows on different devices
- Check that security-critical UI elements are accessible

#### Quick Exercise (5 minutes)

**Everyone try this:**
1. Go to any major e-commerce website
2. Enter responsive design mode (Ctrl+Shift+M)
3. Test these device sizes:
   - iPhone SE (small mobile)
   - iPad (tablet)
   - iPhone 14 Pro (large mobile)
4. Try to complete a task (like adding something to cart) on each size
5. Notice what works well and what doesn't

**[After 5 minutes]**

"What differences did you notice between device sizes? Any surprises?"

---

## Hour 3: Advanced Features & Real-World Scenarios (60 minutes)

### Security & Application Analysis (20 minutes)

**[Switch to Security tab]**

"Let's talk about the Security and Application panels - these are goldmines for understanding how websites really work.

#### Security Panel Deep Dive

**[Navigate to an HTTPS site]**

The Security panel tells you immediately:
- Is this connection secure?
- Is the certificate valid?
- Are there any mixed content issues?

**[Point to security indicators]**

Green = Good, Red = Problems, Yellow = Warnings

**[Click 'View certificate']**

This shows you who issued the certificate and when it expires. Critical for InfoSec teams!

**[Navigate to a site with mixed content issues]**

Mixed content warnings appear here when HTTPS sites load HTTP resources - a common security issue.

#### Application Panel - The Data Detective

**[Switch to Application tab]**

This panel shows you everything a website stores on your computer:

**Storage Types Explained:**

**[Expand Local Storage]**
- **Local Storage**: Permanent data (until manually cleared)
- Common use: User preferences, shopping cart contents

**[Expand Session Storage]**
- **Session Storage**: Temporary data (cleared when tab closes)
- Common use: Form data, temporary UI state

**[Expand Cookies]**
- **Cookies**: Small data files with expiration dates
- Common use: Login status, tracking, personalization

**[Click on a cookie to show details]**

Look at cookie details:
- **Secure**: Only sent over HTTPS (good for security)
- **HttpOnly**: Not accessible to JavaScript (prevents XSS attacks)
- **SameSite**: Controls cross-site request handling

#### Service Workers & PWAs

**[Navigate to a site with service workers]**

Service Workers enable:
- Offline functionality
- Push notifications
- Background sync

**[Show Cache Storage if available]**

This shows what's cached for offline use.

#### Practical Security Analysis

**For InfoSec Teams:**

**[Demonstrate each point]**

1. **Cookie Security Audit:**
   - Check for missing 'Secure' flags
   - Look for overly broad cookie domains
   - Verify sensitive cookies are HttpOnly

2. **Data Storage Review:**
   - What personal data is stored locally?
   - Are passwords or tokens visible?
   - Check for sensitive data in plain text

3. **Third-Party Analysis:**
   - What external domains store data?
   - Are tracking pixels properly configured?
   - Any unexpected data collection?

#### Marketing Applications

**For Marketing Teams:**

**[Show Google Analytics cookies]**

1. **Tracking Verification:**
   - Are your analytics cookies present?
   - Check UTM parameter storage
   - Verify conversion tracking data

2. **Personalization Data:**
   - See what user preferences are stored
   - Check A/B test assignments
   - Review customer journey data

#### Hands-on Exercise (8 minutes)

**Security-Focused Exercise:**
1. Go to your online banking site (or any major secure site)
2. Check the Security panel - is everything green?
3. Go to Application → Cookies
4. Look for cookies with 'Secure' and 'HttpOnly' flags
5. Check Local Storage - is any sensitive data visible?

**Marketing-Focused Exercise:**
1. Go to an e-commerce site
2. Add something to your cart
3. Check Application → Local Storage for cart data
4. Look for Google Analytics cookies
5. Clear all storage and see what happens to your cart

**[Walk around helping participants]**

### Performance Auditing & Lighthouse (15 minutes)

**[Switch to Lighthouse tab]**

"Lighthouse is like having a website expert who gives you a full report card on your site.

#### Understanding Lighthouse

Lighthouse audits five categories:
- **Performance**: How fast does it load?
- **Accessibility**: Can everyone use it?
- **Best Practices**: Is it built well?
- **SEO**: Will Google find it?
- **Progressive Web App**: Does it work offline?

#### Running Your First Audit

**[Click 'Generate report' on a website]**

**[Wait for results, explain while it runs]**

Lighthouse is actually loading your page multiple times, testing different conditions, and measuring everything.

#### Reading the Results

**[Point to each score]**

Scores are 0-100:
- **90-100**: Excellent
- **50-89**: Needs improvement
- **0-49**: Poor

**[Click on Performance section]**

Performance metrics explained:
- **First Contentful Paint**: When users see something
- **Largest Contentful Paint**: When the main content loads
- **Cumulative Layout Shift**: How much the page jumps around

#### Actionable Recommendations

**[Scroll through recommendations]**

Lighthouse doesn't just score - it tells you how to improve:
- Specific issues found
- Estimated time savings
- Links to documentation

#### Role-Specific Lighthouse Uses

**For Marketing:**
- **SEO score**: Will Google rank this page well?
- **Performance score**: Will users convert or bounce?
- **Accessibility score**: Are you excluding potential customers?

**For Developers:**
- **Performance opportunities**: What to optimize first
- **Best practices violations**: Code quality issues
- **PWA checklist**: Modern web app features

**For InfoSec:**
- **Best practices**: Security-related recommendations
- **HTTPS usage**: Secure connection verification

#### Quick Lighthouse Exercise (5 minutes)

**Everyone try this:**
1. Go to your company website (or a competitor's)
2. Run a Lighthouse audit
3. Look at the overall scores
4. Find one specific recommendation you could act on
5. Compare results with a neighbor

### Debugging & Advanced Techniques (15 minutes)

**[Switch to Sources tab]**

"The Sources panel is where developers do deep debugging, but there are features here that benefit everyone.

#### Sources Panel Overview

**[Show the file tree]**

Left side shows all files that make up the website:
- HTML files
- CSS stylesheets  
- JavaScript files
- Images and other assets

#### Basic Debugging Concepts

**[Set a breakpoint by clicking a line number]**

A breakpoint is like saying 'pause here so I can look around.'

**[Trigger the breakpoint and show the paused state]**

When paused, you can:
- See variable values
- Step through code line by line
- Understand what's happening

#### Command Menu - The Power User's Tool

**[Press Ctrl+Shift+P]**

This is the command menu - it gives you access to everything:

**[Type 'screenshot' and show options]**

- Full page screenshots
- Specific area screenshots
- Mobile device screenshots

**[Type 'coverage' and show code coverage]**

Code coverage shows what CSS and JavaScript is actually being used vs. what's loaded.

**[Type 'rendering' and show rendering options]**

Rendering tools help identify:
- Paint flashing (what's redrawing)
- Layout boundaries
- FPS meter

#### Local Overrides - Test Changes Safely

**[Go to Sources → Overrides]**

Local Overrides let you:
- Replace website files with your own versions
- Test changes without affecting the real site
- Experiment safely

**[Set up a simple override demonstration]**

This is perfect for:
- **Developers**: Testing fixes before deployment
- **Marketing**: Testing copy changes
- **InfoSec**: Testing security patches

#### Advanced Screenshots

**[Use Command Menu → Screenshot]**

DevTools can capture:
- **Full page**: Entire webpage, even parts not visible
- **Visible area**: Just what's on screen
- **Specific node**: Just one element

### Real-World Scenarios & Group Exercise (10 minutes)

"Let's put everything together with real scenarios you'll face in your work.

#### Scenario Setup

**[Divide room into mixed groups of 3-4 people with different roles]**

Each group gets a different scenario. You have 7 minutes to use DevTools to solve it, then we'll share results.

#### Scenario 1: Marketing Crisis
**The Problem**: Your landing page conversion rate dropped 50% last week.

**Your Mission:**
- Check if Google Analytics is firing correctly
- Test the page load speed (should be under 3 seconds)
- Verify the checkout button works on mobile
- Look for any console errors that might break the experience

**Tools to Use**: Network panel, Console, Device testing, Lighthouse

#### Scenario 2: Security Incident
**The Problem**: Users report seeing mixed content warnings on your HTTPS site.

**Your Mission:**
- Identify what HTTP content is loading on the HTTPS page
- Check if any sensitive cookies lack security flags
- Verify the SSL certificate is valid and properly configured
- Document all third-party domains accessing your site

**Tools to Use**: Security panel, Network panel, Application panel

#### Scenario 3: Development Debug
**The Problem**: The website navigation menu isn't working on tablets.

**Your Mission:**
- Test the navigation on different tablet sizes
- Find any JavaScript errors in the console
- Check if the CSS is responding properly to screen size changes
- Verify touch interactions work correctly

**Tools to Use**: Device testing, Console, Elements panel

#### Group Work Time

**[Set timer for 7 minutes, circulate and help groups]**

**[After 7 minutes, call time]**

#### Results Sharing

"Let's hear from each group. What did you discover, and how did DevTools help you solve the problem?"

**[Have each group share 1-2 key findings]**

### Wrap-up & Resources (5 minutes)

#### Key Takeaways by Role

**For Everyone:**
- DevTools is not intimidating - it's just organized information
- The Elements panel is your friend for understanding any webpage
- The Network panel shows you everything about performance and data

**For Developers:**
- Console and Sources panels are your debugging headquarters
- Performance auditing should be part of every project
- Local overrides let you test safely

**For Marketing:**
- Network panel verifies tracking and measures performance
- Device testing ensures mobile conversion optimization
- Lighthouse gives you SEO and performance insights

**For InfoSec:**
- Security and Application panels reveal data handling practices
- Network monitoring shows all data transfers
- Cookie analysis helps identify privacy and security issues

#### Next Steps

1. **Practice**: Use DevTools on 3-5 different websites this week
2. **Explore**: Try features we didn't cover using the Command Menu
3. **Apply**: Use DevTools for one real work problem this month

#### Resources for Continued Learning

- **Official Documentation**: https://developers.google.com/web/tools/chrome-devtools
- **Chrome DevTools Tips**: https://umaar.com/dev-tips/
- **Performance Auditing Guide**: Web.dev performance section
- **Security Testing**: OWASP testing guide

#### Final Q&A

"What questions do you have? What would you like to explore more?"

**[Take final questions]**

#### Course Evaluation

"Thank you for three hours of great engagement! Please take 2 minutes to fill out the feedback form - your input helps me improve future workshops."

**[Distribute evaluation forms or provide digital link]**

"Remember - DevTools is now in your toolkit. Don't be afraid to click around and explore. The worst thing that can happen is you refresh the page and start over. Happy debugging!"

---

## Instructor Notes

### Timing Management
- Keep strict time limits - each section builds on the previous
- If running behind, skip the advanced debugging section rather than rushing core concepts
- Build in 2-3 minutes buffer time in each major section

### Audience Management
- Watch for glazed looks during technical sections - pause and check understanding
- Encourage questions throughout, don't wait for designated Q&A times
- Mix up interaction styles: individual work, pair sharing, full group discussion

### Technical Troubleshooting
- Have backup plan if live demos fail (screenshots of expected results)
- Prepare common issues students might face and solutions
- Designate helper volunteers if available

### Differentiation Strategies
- Provide "bonus" exercises for faster learners
- Offer simplified alternatives for struggling participants  
- Use role-specific examples throughout to maintain relevance

### Materials Checklist
- [ ] Sample websites bookmarked and tested
- [ ] Cheatsheet handouts printed
- [ ] Evaluation forms ready
- [ ] Timer or stopwatch
- [ ] Backup presentation slides
- [ ] Contact information for follow-up questions

### Success Metrics
- Participants can open DevTools confidently
- Each role group can identify 2-3 specific use cases for their work
- 80% of participants complete the final scenario exercise successfully
- Positive feedback on practical applicability