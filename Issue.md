---
search: ""
searchDate: ""
modified: 2025-10-17T11:23:44+08:00
---
# Issues
```dataviewjs
await dv.view("plugins/Issue Tracker/IssueTracker", {
    obsidian: obsidian,

    /** Options here */

    // Name of project, used as display text of project note's link
    // project_name: <your project name>,

    // Title of project note, used to find the project note
    // project_note: <project note name>,

    // Sub-folder where issue notes go
    issue_folder: "0 issues/",

    // Template name, a template that exists in your templater folder
    // issue_template: "note.issue-tracker.issue.md",

    // Default query that shows up in the search bar
    // default_query: "is:open",
});
```