---
title: Contributing to the website
description: Anyone can contribute to the website. Whether it is [reporting an issue](#how-do-i-report-an-issue) or [writing content](#how-do-i-edit-content), any help in keeping the website up to date and relevant is helpful. This page explains how.
background: /assets/images/patrice-bouchard-Wq0tdsvq5_4-unsplash.jpg
permalink: /contribute/
---

The follownig content is adapted from [TDWG](https://github.com/tdwg/website).

## Reporting issues

Discovered a typo? Noticed a bug? Have a suggestion to improve a page? Let us know by [creating an issue](https://github.com/atlantichabitatmodels/communityofpractice/issues/new) in the website repository.

### How do I report an issue?

[Click here](https://github.com/atlantichabitatmodels/communityofpractice/issues/new) to report an issue on GitHub. Doing so will automatically notify website maintainers and you will receive an email notification if they have questions or if the issue has been resolved.

Want to solve the issue yourself instead? See [how to edit content](#how-do-i-edit-content).

## Writing content

### How do I edit content?

1. [Browse the website repository](https://github.com/atlantichabitatmodels/communityofpractice) for the page you are looking for.
1. Click the pencil button on the top right to edit the page. You need to be logged-in to GitHub to do this.

    ![Edit button on GitHub](https://www.tdwg.org/static/pages/about/website-faq/edit-page-button.png)

    Note: behind the scenes, this will fork the website repository to your account, so you can make suggestions.

2. Edit the file using [Markdown syntax](https://guides.github.com/features/mastering-markdown/).
3. Preview your suggestions by switching to the `Preview changes` tab. You can switch between the tabs `Edit file` / `Preview changes` as much as you want.
4. At the bottom of the page, write a short description of what you changed.
5. Click the green buttons `Propose file change`, then `Create pull request` and then `Create pull request` again.
6. Great! Your **proposed changes** are now submitted as a [pull request](https://help.github.com/articles/about-pull-requests/) and the website maintainers have been notified. You will receive an email notification if they have questions or when your suggestions have been accepted.

### Do I need to login to edit content?

Anyone can suggest changes using a [GitHub](https://github.com/atlantichabitatmodels/communityofpractice) account, where the authentication and review process is handled.


### How is content organized?

Content is organized in a [hierarchical directory structure](https://github.com/atlantichabitatmodels/communityofpractice), which represent the different sections of the website:

```
content
├── pages
│   ├── best-practices-wg    : Landing page for best practices working group
│   ├── contact              : Information about the mailing list and Slack channel
│   ├── contribute           : This page
│   ├── data-sharing-wg      : Landing page for data sharing working group
│   ├── directory            : Community directory
│   ├── home                 : Home page
│   ├── meetings             : A landing page for all upcoming meetings
│   ├── past-meetings        : A landing page for all past meetings
│   ├── resources            : A place to collect and curate relevant resources
│   └── team                 : Logistics team contact info
│
└── _posts                   : Blog posts
└── assets                   : A place to store image files or other document types
```

### How do I start a new page?

1. Browse the [website repository](https://github.com/atlantichabitatmodels/communityofpractices) to the place where you want to create the page. See [how content is organized](#how-is-content-organized).
2. Click `Create new file`. You need to be logged-in to GitHub to do this.

    ![Create button on GitHub](https://www.tdwg.org/static/pages/about/website-faq/create-page-button.png)

3. Name your file `pages/page-name.md`. File names should be short, lowercase and hyphen-separated.

    ![Name file](https://www.tdwg.org/static/pages/about/website-faq/create-page-name.png)

4. Copy and adapt the following content:

        ---
        title: Page title
        description: Page summary
        background: 
        permalink: page-title-url
        ---

        Page content


5. End your page with an empty line.
6. At the bottom of the page, write a short description of what you changed.
7. Click the green buttons `Propose new file`, then `Create pull request` and then `Create pull request` again.
8. Great! Your **proposed page** is now submitted as a [pull request](https://help.github.com/articles/about-pull-requests/) and the website maintainers have been notified. You will receive an email notification if they have questions or when your suggestions have been accepted.
