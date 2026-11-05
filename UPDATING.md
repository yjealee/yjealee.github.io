# How to update your site

Everything lives in this GitHub repo. To change something: open the file on GitHub, click the pencil icon, edit, then click the green "Commit changes" button. Committing is how you save. There is nothing else to install or push.

While the repo is private, edits are saved but not published. See "Going live" at the bottom.

## Where things are

| I want to change... | Open this file |
|---|---|
| My bio (the paragraph on the home page) | `content/_index.md` |
| Papers (Research tab and home page) | `data/papers.yaml` |
| Teaching tab | `data/teaching.yaml` |
| Miscellaneous tab (blank for now) | `content/miscellaneous.md` |
| Name, title, research interests, email | `hugo.yaml` (the `params:` part) |
| My CV | replace `static/files/cv.pdf` (keep the same name) |
| My photo | replace `static/photo.jpg` (keep the same name) |
| Colors | `assets/css/style.css` (the first block) |

## Change the bio
Open `content/_index.md`. Replace the paragraph. Commit.

## Add or edit a paper
Open `data/papers.yaml`. Copy an existing entry, paste it below, and edit. Keep the spaces at the start of each line exactly as they are.

```yaml
- title: "Paper Title"
  status: "working paper"      # working paper | work in progress | under review | revise and resubmit | accepted | published
  coauthors: ["First Last"]
  venue: ""                    # journal name, once published
  note: ""                     # e.g. "Master's Thesis"
  abstract: "One paragraph."   # appears as a click-to-expand "Abstract"
  pdf: "files/paper-slug.pdf"  # upload the PDF to static/files/ first
```

Papers are grouped by status automatically. To mark a paper published, change `status` to `"published"` and fill in `venue`.

## Write on the Miscellaneous tab
Open `content/miscellaneous.md`. Type below the second `---` line. You can write plain text. Use `## Heading` for a heading and `- item` for a bullet list.

## Replace the CV or photo
Open the folder (`static/files`, or `static` for the photo), click Add file, then Upload files, and drag in the new file with the exact same name. Commit.

## Going live
The automatic publishing is paused (it only runs by hand) so you don't get error emails while the repo is private. When you are ready: make the repo public (Settings, then General, then "Change visibility"), turn on Settings, then Pages, with Source set to "GitHub Actions", and ask Claude to switch the automatic publishing back on. After that, every commit goes live in about two minutes at https://yjealee.github.io/.

## If something breaks
Open the file's History (clock icon) and restore the earlier version, or tell Claude what you changed.
