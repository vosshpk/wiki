# Use

This guide is for people who are new to the Voss HPK wiki.

## Find your way around

- Open a group in the sidebar to see the pages it contains.
- Use search when you are looking for a word, place or document.
- Use the locale selector at the top to switch between Nynorsk and English.
- Choose **Browse** if you prefer to navigate through the folder structure.

Click a page link to open it, then use the headings to find your way through its content.

## Folders and navigation are different things

A page folder determines where wiki pages are stored and what page path they have.
The navigation menu is a separate collection of headings, links and submenus in the sidebar.
A folder does not automatically create a navigation group, and a navigation group does not move pages.
For example, you can save a page at `new-folder/new-page` without creating a matching group in the sidebar.

An automated navigation job reads pages stored in the wiki and creates menu links for them.
New top-level folders that are listed in the navigation group configuration appear under their assigned group when that group exists in the sidebar.
Nested folders and pages appear under the menu link for their parent folder when it has a landing page.
If a folder is not mapped to a navigation group, it appears under **Ungrouped**.
Root-level pages that are not mapped to a group also appear under **Ungrouped**.
If a folder has no landing page, its pages appear as direct links with the folder path in each link label.
**Ungrouped** is an expandable folder below Help with a divider above it, and both the folder and divider disappear when no links remain beneath it.
The menu updates automatically after the saved page content has synchronized, so it can take a few minutes for changes to appear.
The navigation job preserves the placement of menu links that already exist.
If an existing link needs a different placement, an editor must move it in Wiki.js.
If a new folder should appear automatically in a new or existing group, the wiki maintainer must add its path to the technical group list.

## Create a page and folder at the same time

Click the plus button in the top right of Wiki.js and choose **New Markdown Page**.

![The menu for choosing New Markdown Page to create a page](https://raw.githubusercontent.com/vosshpk/wiki/main/assets/help/pages/create-new-page-menu.png)

Open the **Save As** dialog to choose where the page will live.
Select the parent folder, or select the root folder if you want to create a new top-level folder.
Use **New Folder** in the folder tree and enter the name of the new folder.
Enter the page title and a short page path using lowercase letters and hyphens, for example `new-folder/new-page`.
Leave `nn/` or `en/` out of the page path because Wiki.js uses the selected language.
Save the page in the new folder so that the folder contains a page and appears in the content.

![The Save As dialog for choosing a page path and creating a new folder](https://raw.githubusercontent.com/vosshpk/wiki/main/assets/help/pages/create-page-and-folder.png)

A wiki page folder appears in the content repository when it contains at least one saved page.
To upload images or other media files, choose **Upload Media Asset** from the plus menu.

### Create the folder first

Use **New Folder** in the page path tree and choose its parent folder.
Create a page in the new folder or move an existing page into it.
An empty folder is not included in the content repository or navigation menu because the navigation job builds the menu from saved pages.

## Move a page into a folder

Open the page tree or page list, then open the action menu for the page you want to move.
Choose **Rename / Move Page...** and enter the new page path with the folder first.
Check the page title and path before saving the move.
When the page path changes, check links to that page from other pages and documents.
The navigation job updates its menu links after the new page path has synchronized.

![A wiki page action menu with the Rename / Move Page option](https://raw.githubusercontent.com/vosshpk/wiki/main/assets/help/pages/page-rename-or-move.png)

## Create or change a navigation group

Navigation groups are edited in Wiki.js, separately from page folders.
Choose **Edit Nav** at the bottom of the sidebar, then open **Edit Menu Items** for the shared menu.
If Wiki.js shows the navigation settings, edit the menu inherited by pages across the wiki.

![The sidebar with the Edit Nav button at the bottom](https://raw.githubusercontent.com/vosshpk/wiki/main/assets/help/navigation/sidebar-help-and-edit-navigation.png)

![Settings for editing the shared navigation menu](https://raw.githubusercontent.com/vosshpk/wiki/main/assets/help/navigation/edit-navigation-settings.png)

Click **Add** to see the item types **Header**, **Link**, **Menu** and **Separator**.

![The Add button in the navigation editor](https://raw.githubusercontent.com/vosshpk/wiki/main/assets/help/navigation/add-navigation-item-button.png)

![The menu for adding a Header, Link, Menu or Separator](https://raw.githubusercontent.com/vosshpk/wiki/main/assets/help/navigation/add-navigation-item-types.png)

Use **Header** to create the name of a navigation group.
Do not use the **Menu** item type for this kind of group because the navigation job uses headers and nested links.
Use **Link** to create a clickable link or an expandable parent for a submenu.
For an expandable parent, choose **Link (as trigger)**, enter a target page if the group has a landing page, and set the icon to `mdi:folder-outline`.
The navigation job sets this folder icon on folder links it recognizes, including links that already exist in the menu.
Place page links below this parent and use **Nest Item** to make them submenu items.
If the links should appear directly under a heading without an expandable folder, add them after the heading without nesting them.

![Link settings and the option for nesting an item](https://raw.githubusercontent.com/vosshpk/wiki/main/assets/help/navigation/link-trigger-and-nesting.png)

Save the menu items and navigation settings when you are done.
The navigation job keeps existing headings and link placements, but uses the group list to place new links.
For new pages in a folder to go directly into a particular group, give the wiki maintainer the exact group label and folder path.
If the folder is not mapped, or its configured group does not exist in Wiki.js, new links appear under **Ungrouped**.

## File Manager

File Manager shows the wiki page folders and the pages they contain.
Use it to browse the page hierarchy and manage pages and folders.
Open a page editor, open the tools menu in the top right, and choose **File Manager**.

![The page editor menu with the File Manager option](https://raw.githubusercontent.com/vosshpk/wiki/main/assets/help/pages/open-file-manager.png)

![File Manager showing the folder list and wiki pages](https://raw.githubusercontent.com/vosshpk/wiki/main/assets/help/pages/file-manager-overview.png)

Select the parent folder and use **New Folder** to create a wiki page folder.
Open a page's action menu and choose **Rename / Move Page...** to rename or move that page.
Open a folder's action menu and choose **Rename** or **Move** to rename or move the folder.
When you move a folder, its pages move with it and get new page paths.
Check links to pages after changing the path of a page or folder.
To upload images or other media files, choose **Upload Media Asset** from the plus menu.

For more about the group list and the technical navigation job, see [Infrastructure](/en/help/infrastructure).

## Edit and contribute

You can edit a page if your groups give you write access.
Choose **Edit** to open the editor.
Use the toolbar to add headings, lists and links.
Preview the page if that option is available, then save when you are ready.
Open the page in its normal view to check that the change looks right.
Page history shows earlier versions and lets you compare changes.
Contributors can create and edit pages, but cannot move or delete them.
Ask an editor for help if a page needs to be moved or deleted.
Keep the Nynorsk and English content in step when a page exists in both languages.

## Who can do what?

| Group | What you can do |
| --- | --- |
| Guests | Can read pages only. |
| Contributors | Can read, create and edit pages, upload files and submit feedback. |
| Editors | Can edit, review, move and delete pages, and manage navigation. |
| Administrators | Manage Wiki.js settings, users, groups and operations. |

Contributors cannot review submissions, move or delete pages, or manage navigation.
Your access depends on the groups you belong to, and some pages may have their own access rules.
Ask an editor if you are unsure what you can do.
