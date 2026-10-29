# Infrastructure

This page explains where the wiki content is stored and what the technical services do.
It is intended for technically curious readers and people who maintain the wiki.

## How content is updated

Page text is stored as Markdown files in the [vosshpk/wiki GitHub repository](https://github.com/vosshpk/wiki).
GitHub is a service for storing files, tracking changes and collaborating on projects.
Markdown is a simple text format for headings, lists, links and tables.
Wiki.js uses Git Storage to synchronize pages between the wiki and the main branch in GitHub.
Synchronization runs on a schedule that is currently set to every five minutes.
GitHub Actions runs the navigation script when pages change, and the script waits for the content to sync before updating the sidebar.
The script places new top-level folders that are not listed in a configured navigation group under **Ungrouped**.
If such a folder has no landing page, its pages appear as direct links with the folder path in each link label.
Pages stay at their original paths; **Ungrouped** is a sidebar group, not a physical folder.

## What the services do

| Name | Explanation |
| --- | --- |
| Wiki.js | The software that displays the wiki and lets members read and edit pages. |
| Git | Technology that tracks file changes and makes earlier versions available. |
| GitHub | Stores page files in the vosshpk/wiki repository and keeps their change history. |
| Git Storage | The Wiki.js feature that synchronizes page content with GitHub. |
| GitHub Actions | Automation that runs the navigation script after page files change. |
| Markdown | The text format used to write the pages. |
| Docker | Runs Wiki.js and the database as isolated services on the virtual machine. |
| Google Cloud VM | A virtual machine in Google Cloud that runs the wiki. |
| Caddy | Receives HTTPS traffic and forwards it to Wiki.js. |
| PostgreSQL | The database that stores users, settings and uploaded files on a separate persistent disk. |
| Cloud Storage | Private storage where daily database backups are kept for 30 days. |

Wiki.js and PostgreSQL run as Docker services on a virtual machine in Google Cloud.
Caddy receives secure HTTPS traffic from the browser and forwards requests to Wiki.js.
Page text is stored in GitHub, while users, settings and uploaded files are stored in the database.
GitHub Actions updates the navigation through the Wiki.js API after Git Storage has imported the content.
A daily database backup is stored in private Cloud Storage and deleted after 30 days.
The active installation runs Wiki.js 3, which is still in beta.

## Navigation automation group

The group GitHub actions navigation automation is used by the API key that updates the sidebar.
It is a technical automation group, not a group for regular wiki users.

## Detailed group permissions

Contributors can assign tags, view page history, upload and manage files, write their own comments and submit feedback.
They cannot review submissions, move or delete pages, manage navigation, use CSS or JavaScript, or manage other people's comments.
Editors can read, create, edit, review, move and delete pages, assign tags, view page history, manage navigation, files and comments, use CSS and JavaScript, and submit feedback.
Administrators manage Wiki.js settings, users, groups and operations.

## Architecture

::block-plantuml
```plantuml
@startuml
left to right direction

actor "Member or guest" as User
cloud "GitHub\nvosshpk/wiki · main" as GitHub
rectangle "GitHub Actions\nnavigation script" as Actions
cloud "Private Cloud Storage\n30 days" as Backups

node "Google Cloud VM" {
    rectangle "Caddy\nHTTPS proxy" as Caddy
    rectangle "Wiki.js 3\nDocker service" as Wiki
    database "PostgreSQL 18\npersistent disk" as PostgreSQL
}

User --> Caddy : HTTPS
Caddy --> Wiki : forwards request
Wiki <--> GitHub : Git Storage\nMarkdown sync
GitHub --> Actions : page change
Actions --> Wiki : updates the sidebar\nthrough the API
Wiki <--> PostgreSQL : users, settings\nand uploaded files
PostgreSQL --> Backups : daily database backup
@enduml
```
::
