# Chrome DevTools Homework: CSWG Site Analysis

## Overview
Complete these exercises using the Community Systems Working Group website: **https://cswg.infrastructures.org/**

Each exercise builds your DevTools skills while exploring this real organization's website. Document your findings and be prepared to discuss them in our next session.

---

## Exercise 1: Site Structure & Content Analysis (15 minutes)
**Learning Goals**: Master the Elements panel and understand website structure

### Tasks:
1. **Open the CSWG homepage** and launch DevTools (F12)
2. **Navigate the HTML structure**:
   - Use the Elements panel to find the main navigation links
   - Identify how many main sections the page has
   - Find the Discord link and note its target URL

3. **Content Discovery**:
   - Use Ctrl+F (or Cmd+F) in the Elements panel to search for "PromiseGrid"
   - Find where the GitHub repositories link points to
   - Locate the "fundamental limitations" link and see where it leads

4. **Visual Modifications** (practice only - changes won't save):
   - Change the main heading color to red
   - Add a yellow background to the "Goals" section
   - Hide the "Contact Us" section entirely

### Deliverables:
- Screenshot of your color changes
- List of all external links found on the page
- Note which HTML tags are used for the main sections

---

## Exercise 2: Performance & Network Analysis (20 minutes)
**Learning Goals**: Analyze loading performance and network requests

### Tasks:
1. **Baseline Performance**:
   - Open Network panel and refresh the page
   - Record the total load time and number of requests
   - Identify the largest file being loaded

2. **Mobile Performance Testing**:
   - Enable Device Mode (Ctrl+Shift+M)
   - Test the site on iPhone SE and iPad
   - Use "Slow 3G" throttling and refresh
   - Record mobile load times vs desktop

3. **Resource Analysis**:
   - Filter Network panel by file type (JS, CSS, Images)
   - Identify any external domains being contacted
   - Check if there are any failed requests (404s)
   - Look for any third-party tracking or analytics

4. **Lighthouse Audit**:
   - Run a full Lighthouse performance audit
   - Note the Performance, SEO, and Accessibility scores
   - Identify the top 3 recommendations for improvement

### Deliverables:
- Performance comparison table (Desktop vs Mobile vs Slow 3G)
- List of all external domains contacted
- Screenshot of Lighthouse scores with key recommendations highlighted

---

## Exercise 3: Security & Privacy Investigation (15 minutes)
**Learning Goals**: Use Security and Application panels for privacy/security analysis

### Tasks:
1. **Security Assessment**:
   - Check the Security panel - is the site properly secured?
   - Verify the SSL certificate details
   - Look for any mixed content warnings

2. **Data Storage Analysis**:
   - Examine Local Storage, Session Storage, and Cookies
   - Document what data (if any) the site stores locally
   - Check if the site uses any tracking technologies

3. **Third-Party Analysis**:
   - Use Network panel to identify all third-party services
   - Check what data might be shared with external services
   - Note any privacy implications

### Deliverables:
- Security assessment summary (secure/not secure and why)
- List of any stored data found
- Privacy analysis of third-party connections

---

## Exercise 4: Console Investigation & Link Testing (15 minutes)
**Learning Goals**: Use Console for debugging and information gathering

### Tasks:
1. **Console Inspection**:
   - Check for any JavaScript errors or warnings in Console
   - Test these Console commands and document results:
     ```javascript
     document.title
     location.href
     document.links.length
     window.navigator.userAgent
     ```

2. **Link Validation**:
   - Use Console to extract all links: `Array.from(document.links).map(l => l.href)`
   - Manually test the external links (GitHub, Discord, etc.)
   - Check if any links are broken or redirect

3. **Content Analysis**:
   - Use Console to count specific elements:
     ```javascript
     document.querySelectorAll('h1, h2, h3').length
     document.querySelectorAll('a').length
     document.body.innerText.split(' ').length
     ```

### Deliverables:
- List of Console command results
- Status report on all external links (working/broken)
- Word count and heading structure summary

---

## Exercise 5: Accessibility & User Experience Analysis (15 minutes)
**Learning Goals**: Evaluate site accessibility and mobile experience

### Tasks:
1. **Accessibility Check**:
   - Run Lighthouse Accessibility audit
   - Use Elements panel to check if images have alt text
   - Verify heading hierarchy (H1, H2, H3 proper order)
   - Check color contrast in DevTools

2. **Mobile User Experience**:
   - Test site navigation on various mobile devices
   - Check if all links are easily clickable on touch devices
   - Verify text readability at different zoom levels
   - Test horizontal scrolling behavior

3. **Content Structure Analysis**:
   - Evaluate information hierarchy
   - Check if the site achieves its stated goals
   - Assess clarity of navigation and calls-to-action

### Deliverables:
- Accessibility score and top issues found
- Mobile UX assessment with specific recommendations
- Evaluation of how well the site serves its target audience

---

## Exercise 6: Advanced Investigation - GitHub Integration (20 minutes)
**Learning Goals**: Follow external links and analyze connected resources

### Tasks:
1. **GitHub Repository Analysis**:
   - Follow the GitHub organizations link from the CSWG site
   - Use DevTools on the GitHub page to:
     - Find the PromiseGrid repository
     - Count how many repositories the organization has
     - Check the last update dates

2. **Cross-Site Comparison**:
   - Compare network performance between CSWG site and GitHub
   - Analyze the different security configurations
   - Note differences in tracking/analytics between the sites

3. **Integration Assessment**:
   - Evaluate how well the CSWG site integrates with its external resources
   - Check if Discord invite link works properly
   - Assess the user journey from CSWG site to project resources

### Deliverables:
- Comparison chart of CSWG vs GitHub performance
- Analysis of the complete user journey to project resources
- Recommendations for improving external link integration

---

## Bonus Challenge: Site Improvement Recommendations (10 minutes)
**Learning Goals**: Synthesize findings into actionable recommendations

### Tasks:
1. **Overall Assessment**:
   - Based on all your DevTools investigations, identify the site's strengths
   - List the top 3 areas for improvement
   - Consider the site's goals and target audience

2. **Technical Recommendations**:
   - Suggest specific performance improvements
   - Recommend accessibility enhancements
   - Propose security or privacy improvements

3. **User Experience Suggestions**:
   - Evaluate information architecture
   - Suggest navigation improvements
   - Recommend content or design changes

### Deliverables:
- Executive summary of site assessment
- Prioritized list of technical improvements
- UX recommendations with rationale

---

## Submission Guidelines

### What to Submit:
1. **Screenshot collection** showing your DevTools work
2. **Written report** (1-2 pages) covering:
   - Key findings from each exercise
   - Performance and security assessment
   - Recommendations for improvement
3. **Reflection paragraph** on:
   - Which DevTools features you found most useful
   - What surprised you about the site
   - How you might apply these skills to your work

### Format:
- Create a simple document (Word, Google Docs, or PDF)
- Include screenshots with clear labels
- Use bullet points for findings and recommendations
- Be specific about numbers, metrics, and observations

### Due Date:
Submit by [INSERT DATE] via [INSERT METHOD]

---

## Learning Outcomes Checklist

After completing these exercises, you should be able to:
- [ ] Navigate any website's HTML structure using Elements panel
- [ ] Analyze website performance and identify bottlenecks
- [ ] Assess security and privacy implications of websites
- [ ] Use Console for basic website investigation
- [ ] Evaluate accessibility and mobile user experience
- [ ] Follow external integrations and assess user journeys
- [ ] Synthesize technical findings into business recommendations

---

## Additional Resources

- **CSWG Context**: This is a real working group focused on decentralized infrastructure
- **Technical Background**: Open-source communities often prioritize functionality over polish
- **Analysis Lens**: Consider how technical choices support the organization's mission
- **Professional Application**: Practice translating technical findings into actionable insights

**Questions?** Bring specific DevTools questions or interesting findings to our next session!

---

## Instructor Notes

### Why This Site Works Well for Homework:
- **Simple structure** allows focus on DevTools rather than complex content
- **Real organization** provides authentic context and meaningful analysis
- **External integrations** (GitHub, Discord) teach cross-site analysis
- **Open-source context** appeals to technical learners
- **Performance-focused** organization makes optimization analysis relevant

### Expected Student Challenges:
- Understanding GitHub organizational structure
- Interpreting Lighthouse recommendations
- Connecting technical findings to business implications

### Extension Opportunities:
- Compare CSWG site to similar organizations
- Analyze the linked academic papers
- Investigate the PromiseGrid project documentation