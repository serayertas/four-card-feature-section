Frontend Mentor - Four card feature section solution

This is a solution to the Four card feature section challenge on Frontend Mentor. Frontend Mentor challenges help you improve your coding skills by building realistic projects.

Table of contents
Overview
The challenge
Links
My process
Built with
What I learned
Continued development
AI Collaboration
Author
Overview
The challenge

Users should be able to view the optimal layout for the site depending on their device's screen size.

Links
- Solution URL: [GitHub Repo](https://github.com/serayertas/four-card-feature-section)
- Live Site URL: [Live Site](https://serayertas.github.io/four-card-feature-section/)
My process
Built with
Semantic HTML5 markup
CSS Grid
Flexbox
Media queries for a responsive layout
Google Fonts (Poppins)
What I learned

This project's main challenge was the staggered card layout, where the Supervisor and Calculator cards need to sit centered next to the Team Builder and Karma cards stacked on top of each other. My first attempt used CSS Grid row-spanning (grid-row: 1 / 3) combined with align-self: center, but the row track sizing behaved unpredictably. I ended up with a more reliable structure: wrapping the two stacked cards in their own container and placing all three columns as simple, equal-height grid items.

css
.cards {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  align-items: center;
  gap: 20px;
}

.middle-column {
  display: flex;
  flex-direction: column;
  gap: 20px;
}

I also learned a simple, reliable way to pin an icon to the bottom-right corner of a card regardless of its height, using position: relative on the card and position: absolute on the icon, instead of fighting with flexbox's margin-top: auto inside a grid item.

Continued development
Get more comfortable predicting how CSS Grid sizes rows/columns with spanning items
Practice building layouts mobile-first instead of adjusting a desktop layout down
AI Collaboration

I used Claude as a mentor while building this project, describing what I was seeing versus what the design expected and working through the layout step by step rather than being handed a finished solution. It was especially helpful for diagnosing why the grid row-spanning approach wasn't producing the expected result, and for suggesting the more reliable absolute-positioning technique for the corner icons.

Author
GitHub - @serayertas