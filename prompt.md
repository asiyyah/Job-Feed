# Prompt Log

## Dec 27, 2025: Nav Bar
**Prompt:** "Create a fixed header nav bar for an AI-Powered Job Search and Application Assistant. The nav bar should include a profile combobox with an avatar leading icon, a chevron down trailing icon and name content, nave links that includes: dashboard, jobs, applications, interview prep and settings, a universal search bar to the right, notification icon and a profile avatar.

The ui should be a monochrome palette of black and white, use soft borders for the search barch and maintain consistent spacing and ui elements"

**Outcome:** Created a nav bar that worked well using variables already created in the file for the styling.

**Prompt 2 (Refinement):** "Add all the html elements into the .container div, group the profile combobox and nav-links in a container (nav-left), maintain a gap of 24 px using the variables already created and maintain consistent spacing between nav-left and nav-right in the header container"

**Outcome:** Created a new container (nav-left), moved specified elements in the prompt to the new container. Styled the new container in css with the specified spacing

**Prompt 3 (Job list card):** Create a job card for the job recommendations list.
The card should contain the hiring company logo, role and company name to the top left, view details button and bookmark icon button to the top right.

The job summary and relevant tags should be in the middle of the card and details of the role (contract type, salary range, role type and when the job was posted ) should be at the bottom of the card.

Since it's an AI powered job search platform, there should be ai job match score and recommendation type (ai match) also at the top of the card

**Outcome:** Partial success. Created a job card based on the prompt.

**Notes:** 
1. The 'AI Match' container has a poor contrast.
2. The card is not set to fill the container, leaving empty white space to the right of the job list container
3. The relevant tags needs to be in a pill tag to create a visual distinction

**Prompt 4 (Refinement):** 
Add a border 100 with border radius lg to the job list container
Make the job card fill it's container, change it's border to border-50
Change ai-match background color to white, make the text color: text-muted, add a border (border-100)
Change the relevant tags to pill shaped tags with paddings p-25 p-o5, add border-100

**Outcome:** Partial success. 
1. Updated the ui with the fixes but the cards are still fitting their contents and overlapping.
2. The pill tags have inconsistent paddings

**Prompt 5 (Refinement):** 
Add a consistent spacing in the job card gap-4. The elements are shrunk together in the card. Do not use margins and stick to the paddings only

**Notes:** 
1. The job card with a shorter job summary fitted it's content and had a smaller width
2. The job card with a longer job summary extended out of it's parent container with a longer width

**Fixes:**
1. Remove Width 100% from job-list and job-card container
2. Changed 'align-items: flex-start' to 'align-items: stretch' in jon-list container. This ensures the child elements (job-card) fill the container irrespective of it's inner contents