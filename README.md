Personal Portfolio Website — IWD Assignment
Student Name: Muyangwa Muyangwa
Student ID: 2601810163
GitHub Repository: https://github.com/Muyangwaa/GRROOMERS/tree/main
Question 1: Website Creation 
-The website is a business/small-business website called GRROOMERS, a mobile dog grooming service. It advertises services 
Elements used (49 distinct tags, well above the 25 minimum):
html, head, meta, title, link, body, a, header, div, h1, p, strong, nav, ul, li, main, section, h2, em, article, h3, aside, details, summary, figure, figcaption, table, caption, thead, tr, th, tbody, td, form, fieldset, legend, label, input, br, textarea, button, select, option, time, hr, footer, dl, dt, dd
Attributes used (24 distinct attributes, above the 15 minimum):
lang, charset, name, content, href, rel, id, role, aria-label, aria-labelledby, tabindex, datetime, scope, type, placeholder, required, autocomplete, value, selected, disabled, rows, method, action, for
Question 2: HTML Elements
Five most challenging elements to implement:
<table> getting <thead>, <tbody>, <th scope="row">/<th scope="col">, and <caption> 
<details>/<summary>  deciding what belongs in the visible summary compared to the collapsible content for each service card.
<form> with mixed input types (text, email, tel, checkbox) plus <select>/<option> coordinating required, placeholder, and autocomplete consistently.
<dl>/<dt>/<dd> were an unfamiliar structure for the "Quick details" contact block, easy to mix up which tag wraps the label verses actual the value.
<figure>/<figcaption>  using them semantically for the gallery even without actual images.(NB.the git repository keeps work available for continuity later)
Semantic structure: <header> holds the site title/nav; <main> wraps all page content; each major topic (intro, services, pricing, gallery, reviews, contact) is its own <section> with a heading tied in via aria-labelledby; each individual service and the review is an <article>, since it's independently meaningful content; <footer>, closes the page with copyright and footer nav.
Most useful for layout: <section> , because it let me break the single page into clearly bounded, independently labeled topic areas (services, pricing, gallery, reviews, contact) that both mirror the nav links and make the outline easy to scan.
Question 3: HTML Attributes
Three essential functional attributes: href (drives all navigation, including the in-page anchor links), id (anchor targets for navigation and <label for> associations), required (enforces that booking-form fields aren't submitted empty).
class vs id: id is used for unique, one-off targets that need to be referenced individually anchor targets like #services, #pricing, #contact, and form field ids like #name/#email (each paired with a <label for>). class is used for repeated elements that share a common pattern but don't need individual identification, e.g. class="service-card" on all four service <article> elements, and class="booking-form" / class="review-form" on the two forms, so they could share styling rules without duplicating unique ids.
Attribute that most improved UX: placeholder on the form inputs, it shows an example of the expected input format (e.g. "e.g., sam@email.com") right in the field, reducing user guesswork before submission.
Question 4: Development Process
Planning: Sketched the page as a list of sections a small grooming business needs — intro/hero, services, pricing, gallery, reviews, contact/booking then matched each to a semantic wrapper (section/article) before writing markup.
Testing/debugging: Opened the file directly in a browser to check that anchor links scrolled to the right sections, that form fields showed correct input types/placeholders, and that the table rendered with correct headers.
Challenges: Structuring the pricing table with proper header scoping, and deciding when to use <article> vs <div> for the service list items. Resolved by treating anything independently reusable/syndicatable as <article> and reserving <div> for layout-only wrapping.
Question 5: Git & GitHub Implementation
Git commands used: git init, git add ., git commit -m "...", git branch -M main, git remote add origin [repo-url], git push -u origin main.
Commits: Committed incrementally by section (e.g. "Add header and nav", "Add services section", "Add pricing table", "Add booking form", "Add footer and final polish") so each commit represented one logical addition.
Why version control matters: It tracks the history of changes, makes it possible to revert mistakes, supports collaboration (instructor as collaborator), and gives a clear audit trail of how the site was built over time.
Question 6: Code Quality & Best Practices
Validity: Checked the markup structure manually against the HTML5 spec (proper nesting, closing tags, single <h1>) and tested in-browser; would run the file through the W3C Markup Validator before final submission.
Best practices followed: Semantic elements over generic <div>s where possible, aria-label/aria-labelledby for accessible section headings, <label for> tied to every form input, consistent indentation.
Improvements with more time: Add class attributes for CSS hooks, fix the malformed markup in the Reviews section (a stray <action="#" method="post"> fragment with no opening <form> tag), add real <img> elements with alt text to the gallery, and wire the form up to an actual backend/mailto: handler.
