Alternate front-end to Hacker News that allows the user to quickly mark
article *titles* as having been "processed" (by the user) without needing the user
to actually have to click on the link and load the associated article.  This allows
the user to quickly identify new (to the user) articles on each page reload, and
can greatly reduce scanning time.

The page remembers the articles that the user had previously marked as "processed"
in localStorage, so it will remember these across page reloads.  The page also cleans
out any remembered "processed" articles from localStorage that are older than 72
hours, on page load, to keep the working set of remembered articles to a 72-hour
window, keeping load and save operations to localStorage nice and fast, and avoiding
exhausting localStorage over long periods of time.
