# How to update your site

Your site is live at https://yjealee.github.io/. Everything lives in this GitHub repo. To change something: open the file on GitHub, click the pencil icon, edit, then click the green "Commit changes" button. Committing is how you save, and the site updates by itself about two minutes later. There is nothing else to install or push.

## Where things are

| I want to change... | Open this file |
|---|---|
| My bio (the paragraph on the home page) | `content/_index.md` |
| Papers (Research tab and home page) | `data/papers.yaml` |
| Intro sentence on the Research tab | `content/research.md` |
| Contact tab | `content/contact.md` |
| Name, title, research interests, email | `hugo.yaml` (the `params:` part) |
| My CV | replace `static/files/cv_long.pdf` (keep the same name) |
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

## Replace the CV or photo
Open the folder (`static/files`, or `static` for the photo), click Add file, then Upload files, and drag in the new file with the exact same name. Commit.

## If something breaks
Open the Actions tab to see whether the last update succeeded. Or open the file's History (clock icon) and restore the earlier version, or tell Claude what you changed.
