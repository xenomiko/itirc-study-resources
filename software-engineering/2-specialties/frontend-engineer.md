# Frontend Engineer

**Role:** builds the interfaces people use in the browser, with attention to usability, accessibility and performance.
**Prerequisites:** [Programming basics](../1-basics/programming-basics.md) and Git.

## Skills, in order
1. HTML and semantic markup
2. CSS: layout, flexbox, grid, responsive design
3. JavaScript fundamentals and the DOM
4. TypeScript
5. A framework: React first
6. Accessibility and performance
7. Testing: unit and end-to-end
8. Build tools and deployment

**Path at a glance:**
- Beginner: MDN Learn Web Development or The Odin Project, then JavaScript.info.
- Intermediate: TypeScript Handbook, React docs, web.dev Learn.
- Advanced: Playwright for end-to-end tests, performance and accessibility audits, Next.js.

## Resources
| Resource | Level | Cost | What it is | You will be able to |
|---|---|---|---|---|
| [MDN Learn Web Development](https://developer.mozilla.org/docs/Learn_web_development) | Beginner | Free | Mozilla's structured path through HTML, CSS and JavaScript. | Build and style a responsive page with semantic HTML. |
| [The Odin Project](https://www.theodinproject.com) | Beginner to Intermediate | Free | Project-based full curriculum with a strong community. | Build several portfolio projects and use Git on each. |
| [JavaScript.info](https://javascript.info) | Beginner to Intermediate | Free | Modern JavaScript tutorial covering the language and the browser. | Use closures, promises, async/await and DOM events correctly. |
| [web.dev Learn](https://web.dev/learn) | Beginner to Intermediate | Free | Google's courses on CSS, accessibility, forms and performance. | Write accessible forms and understand layout and responsive images. |
| [TypeScript documentation](https://www.typescriptlang.org/docs/) | Intermediate | Free | Official handbook and playground. | Add types to a project and catch bugs at compile time. |
| [React: Learn](https://react.dev/learn) | Intermediate | Free | Official tutorial and guides. | Build components with state, props and effects. |
| [Full Stack Open](https://fullstackopen.com/en/) | Intermediate | Free | University of Helsinki course covering React, Node, TypeScript, testing and GraphQL. Also used in [Backend Engineer](backend-engineer.md). | Build and test a full-stack app end to end. |
| [Playwright documentation](https://playwright.dev/docs/intro) | Intermediate to Advanced | Free | Official docs for browser end-to-end testing. | Write reliable tests that drive a real browser. |
| [Next.js Learn](https://nextjs.org/learn) | Intermediate to Advanced | Free | Official course on a popular React framework. | Build a server-rendered app with routing and data fetching. |
| [Frontend Mentor](https://www.frontendmentor.io) | Beginner to Intermediate | Free + paid | Supplementary: design-to-code challenges. Check which are free. | Practice turning designs into responsive pages. |
| [W3C WAI: Web Accessibility Tutorials](https://www.w3.org/WAI/tutorials/) | Intermediate | Free | Supplementary: official guidance on accessible patterns. | Build accessible menus, forms and images. |

## Certifications
No standard certification. A portfolio of deployed projects matters most.

## Project

### Tutorial projects
Each project takes about a week (roughly 8 to 12 hours) and covers several skills from the list above. Do them in order, and keep each one in its own Git repo or folder.

1. **Responsive multi-page site** (Beginner, ~1 week)
   - **Build:** a three-page site with semantic HTML, grid and flexbox layout, a contact form and data fetched from a public API with loading and error states.
   - **Practice:** HTML, CSS layout, responsive design, JavaScript, the DOM.
   - **Done when:** it works from phone to desktop width with no horizontal scrolling and handles a failed API call.
2. **React and TypeScript app** (Intermediate, ~1 week)
   - **Build:** rebuild it in React with TypeScript, routing, typed API calls and unit tests.
   - **Practice:** TypeScript, components, state, effects, testing.
   - **Done when:** strict type checking passes and the main flows have tests.
3. **Accessibility and performance** (Intermediate, ~1 week)
   - **Build:** audit your app with Lighthouse and the W3C WAI tutorials, fix issues, and add Playwright end-to-end tests.
   - **Practice:** accessibility, performance, end-to-end testing, keyboard use.
   - **Done when:** you finish every flow with the keyboard only and Lighthouse scores improve with a documented before and after.

### Final project
**Time:** 3 to 4 weeks. A deployed TypeScript and React (or Next.js) app with realistic features such as listing, search, forms and a mocked API.

**Specific to this project:**
- Unit tests plus Playwright tests running in CI on every pull request.
- A performance budget and accessibility check enforced in CI.
- Error boundaries, user-friendly error states and basic client-side logging.
- Preview deployments for pull requests and short decision notes on your main choices.

Also meets the [production-like bar](../../README.md#what-production-like-means).
