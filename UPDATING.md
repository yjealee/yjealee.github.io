# Updating your site

You can do all of this in the browser on GitHub: open the file, click the pencil icon, edit, then "Commit changes". The site rebuilds and goes live in about two minutes.

## Change your bio
Edit `content/_index.md`. Replace the paragraph (and delete the `<!-- PLACEHOLDER ... -->` line).

## Change tagline, email, or social links
Edit `hugo.yaml` under `params:`. To show a link (Google Scholar, GitHub, LinkedIn, ORCID, X), paste the full URL between the quotes. Leave `""` to hide it.

## Add a paper
Edit `data/papers.yaml` and copy an existing entry. Fields:

```yaml
- title: "Paper Title"
  status: "working paper"      # working paper | work in progress | under review | revise and resubmit | accepted | published
  coauthors: ["First Last"]
  venue: ""                    # journal name, once published
  note: ""                     # e.g. "Master's Thesis"
  abstract: "One paragraph."   # shows as a click-to-expand "Abstract"
  pdf: "files/paper-slug.pdf"  # upload the PDF to static/files/ first
```

Papers are grouped automatically by status. To mark a paper published, change `status` to `"published"` and fill in `venue`.

## Update your CV
Upload the new PDF to `static/files/` named exactly `cv.pdf` (it replaces the old one).

## Add your photo
Upload a headshot to `static/images/` named exactly `photo.jpg`. It appears automatically (portrait, about 800 px wide is plenty). Delete it to hide the photo.

## Add teaching, grants, talks, or service
Edit `data/teaching.yaml`, `data/awards.yaml`, `data/talks.yaml`, or `data/service.yaml`, and copy an existing entry. To remove a whole section, empty its file.

## If your GitHub address changes
Edit `baseURL` in `hugo.yaml`, and the two `https://` addresses in `static/robots.txt` and `static/llms.txt`.

## Change colors
Edit the first block (`:root { ... }`) in `assets/css/style.css`.
