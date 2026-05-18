# README

## Amormio Velasquez III

## Check Your Understanding

1. Where would you fit your automated tests in your Recipe project development pipeline? Select one of the following and explain why.

Answer: Within a Github action that runs whenever code is pushed

This makes it so that the entire team can see how the tests ran (success/failure) and protects the codebase from faulty code when tests fail. Automating it in the CI pipeline will guarantee tests will run, while we can't guarantee devs being disciplined enough to test rigorously locally, and of course we should test throughout development.

2. Would you use an end to end test to check if a function is returning the correct output? (yes/no)

No

3. What is the difference between navigation and snapshot mode?
   Navigation mode will analyze the page after a fresh page load and measure performance and other metrics (which we saw with the 4 categories) during that page load. Snapshot mode is best used for finding accessibility issues because it doesn't analyze from a fresh page load (thus it can't measure performance or other loading behavior), it looks at the page at its current state. So snapshot effectively is suited towards its name, taking a snapshot of the page's current state which may have already been interacted with to test accessibility

4. Name three things we could do to improve the CSE 110 shop site based on the Lighthouse results.
   Based on the results, performance and best practices were rated 100 but accessibility a 90 and SEO a 91.
   We could improve on the following:

- accessbility: add a lang attribute to the html tag, currently assumes that the content is in the user's default language which could pose as a problem if it actually isn't
- seo: add a meta tag with a clear and concise description so the page isn't marked as spam and it's treated as more relevant
- performance: we can reduce unused JS, minify our js files, avoid chaining critical requests to reduce overhead, use more efficient cache times
