---
layout: single
title: "How to Update This Site"
permalink: /how-to-update/
toc: true
toc_sticky: true
---

This guide walks you through how to make changes to the Back2Build website. Everything is done through GitHub's website — no software to install, no coding experience needed.

- **The website:** [https://back2build.github.io/](https://back2build.github.io/)
- **The files (GitHub):** [https://github.com/back2build/back2build.github.io](https://github.com/back2build/back2build.github.io)

## Before You Start

The website files live on GitHub. To make changes:

1. Go to [the repository on GitHub](https://github.com/back2build/back2build.github.io).
2. Sign in to your GitHub account.
3. Navigate to the file you want to change.
4. Make your edits and **commit** (save) them.

**"Commit" just means "save."** When GitHub asks you to "commit changes," it is asking you to save your work. Type a short note describing what you changed (e.g., "Add student Jane Doe") and click the green button.

## Adding a New Student

This is the most common task. Follow these steps:

### Step 1: Upload the student's photo first

See the [Uploading Student Photos](#uploading-student-photos) section below.

### Step 2: Create the student file

1. In GitHub, navigate to the **`_students`** folder.
2. You will see a file called **`_TEMPLATE.md`** — click on it.
3. Click the **"Raw"** button (top-right of the file content) to see the plain text.
4. **Select all** the text and **copy** it.
5. Go back to the `_students` folder.
6. Click **"Add file"** then **"Create new file."**
7. In the filename box at the top, type the student's name in this format: `firstname_lastname.md`
   - All lowercase
   - Underscore between names
   - Must end in `.md`
   - Example: `jane_moyo.md`
8. **Paste** the template you copied.
9. Replace all the UPPERCASE PLACEHOLDER text with the student's real information:
   - `STUDENT FULL NAME` — their full name, e.g., `Jane Moyo`
   - `SCHOOL and FORM/LEVEL` — e.g., `Mpompoma L6`
   - `PHOTO_FILENAME.jpg` — the exact filename of the photo you uploaded (appears in two places, update both)
   - `STUDENT FIRST NAME` — their first name
   - `THEIR MAIN FIELD` — e.g., `Public Health`
   - `SKILL 1, SKILL 2, SKILL 3` — e.g., `Data Analysis, Community Health, Statistics`
10. **Delete** the line that says `published: false` (this line prevents the page from appearing on the site).
11. **Delete** the INSTRUCTIONS block at the bottom.
12. Replace the placeholder bio text with the student's actual bio.
13. Click **"Commit changes"**, type a short description like "Add student Jane Moyo", and click the green **"Commit changes"** button.

### What each field does

| Field | What it controls |
|---|---|
| `title` | The student's name displayed as the page heading |
| `excerpt` | Short subtitle shown under their name on the Students grid |
| `header: teaser` | The thumbnail photo on the Students grid page |
| `sidebar: image` | The larger photo on their individual profile page |
| `sidebar: "Focus Area"` | Their main field of study or work |
| `sidebar: "Skills"` | Their specific skills, separated by commas |
| The text below the `---` | Their full bio, written in plain English |

## Uploading Student Photos

1. In GitHub, navigate to **`assets`** then **`images`** then **`students`**.
2. Click **"Add file"** then **"Upload files."**
3. Drag the photo in or click to browse your computer.
4. **Photo tips:**
   - Name the file something simple like `jane_headshot.jpg` (lowercase, no spaces).
   - Crop to roughly square if possible.
   - Keep the file size under 500 KB. If the photo is from a phone camera, it may be too large — use a free tool to resize it first.
5. Click **"Commit changes."**

**Important:** Upload the photo *before* creating the student file, so the image link works right away.

## Editing an Existing Page

1. Navigate to the file you want to edit (see the [Quick Reference](#quick-reference) table at the bottom).
2. Click the **pencil icon** (top-right of the file content) to enter edit mode.
3. Make your changes.
4. Click **"Commit changes"**, add a short description of what you changed, and save.

### Which file is which page?

| Page on the website | File to edit |
|---|---|
| Homepage | `_pages/home.md` |
| Donation page | `_pages/donate.md` |
| Students grid page (the heading text) | `_pages/student-listing.md` |
| Blog listing page | `_pages/post-listing.md` |

## Editing a Student Profile

1. Navigate to the **`_students`** folder.
2. Click on the student's file (e.g., `nomaqhawe_ncube.md`).
3. Click the **pencil icon** to edit.
4. To change their bio, edit the text below the second `---` line.
5. To change their details (school, skills, photo), edit the fields in the top section between the two `---` lines. Be careful not to remove the colons or change the indentation.
6. Commit your changes.

## Adding a Blog Post

1. Navigate to the **`_posts`** folder.
2. Click **"Add file"** then **"Create new file."**
3. Name the file using this exact format: **`YYYY-MM-DD-short-title.md`**
   - The date must be real and in year-month-day format
   - Use hyphens between words in the title part
   - Example: `2026-04-06-fundraiser-recap.md`
   - **If the date format is wrong, the post will not appear on the site**
4. Paste this template and fill it in:

```
---
title: "YOUR POST TITLE"
categories:
  - News
tags:
  - event
---

Write your post content here.
```

`categories` and `tags` are optional but help organize posts. Use whatever makes sense — common ones might be "News", "Events", or "Updates".

## Editing the Navigation Menu

The menu at the top of the site is controlled by one file: **`_data/navigation.yml`**

It looks like this:

```yaml
main:
  - title: "Home"
    url: /
  - title: "Students"
    url: /students/
  - title: "Donate"
    url: /donate/
```

- To **add** a link: copy two lines (a `title` and `url` pair) and change the values.
- To **remove** a link: delete those two lines.
- **Indentation matters** — use exactly 2 spaces before the dash, and 4 spaces before `title:` and `url:`. Do not use tabs.

## Writing with Markdown

The content on this site is written in **Markdown**, a simple way to format text. Here are the basics:

### Text formatting

```
**bold text**
*italic text*
```

Becomes: **bold text** and *italic text*

### Headings

```
## Big Heading
### Smaller Heading
#### Even Smaller Heading
```

Use `##` for main sections and `###` for subsections. The more `#` symbols, the smaller the heading.

### Links

```
[link text](https://example.com)
```

Becomes: [link text](https://example.com)

### Lists

```
- Item one
- Item two
- Item three
```

Becomes:
- Item one
- Item two
- Item three

For numbered lists:

```
1. First thing
2. Second thing
3. Third thing
```

### Paragraphs

Just leave a blank line between paragraphs. No special formatting needed.

```
This is the first paragraph.

This is the second paragraph.
```

## After You Save

When you commit (save) a change, the site does **not** update instantly. GitHub needs about **1 to 2 minutes** to rebuild the site with your changes.

After saving:
1. Wait about 1-2 minutes.
2. Go to [https://back2build.github.io/](https://back2build.github.io/) and **refresh the page** (Ctrl+R on Windows, Cmd+R on Mac).
3. You should see your changes.

If changes still don't appear after 5-10 minutes, something may have gone wrong — see Troubleshooting below.

## Troubleshooting

**My changes aren't showing up**
- Wait at least 2 minutes and refresh the page. GitHub Pages takes time to rebuild.
- If it has been more than 10 minutes, go to the **"Actions"** tab in GitHub to check for build errors (a red X means something went wrong).

**A student photo is not showing**
- Double-check that the filename in the student file matches the actual photo filename exactly, including capitalization. `Jane_Headshot.jpg` is not the same as `jane_headshot.jpg`.
- Make sure the path starts with `/assets/images/students/`.

**The page looks broken or blank**
- The section between the two `---` lines at the top (called "front matter") is very strict about formatting:
  - Always use **straight quotes** (`"like this"`), not curly/smart quotes ("like this"). If you type in a word processor and paste, the quotes may be wrong.
  - Always put a **space after every colon**. Write `title: "Hello"` not `title:"Hello"`.
  - Do not add or remove spaces at the start of lines in the front matter — the indentation must stay exactly as it is in the template.

**A new blog post isn't appearing**
- The filename must start with a date in `YYYY-MM-DD-` format. Example: `2026-04-06-my-post.md`. If the date is missing or in the wrong format, Jekyll will ignore the file.

## Quick Reference

| What you want to change | Where to find it |
|---|---|
| Homepage content | `_pages/home.md` |
| Student profiles | `_students/firstname_lastname.md` |
| Student photos | `assets/images/students/` |
| Student template | `_students/_TEMPLATE.md` |
| Blog posts | `_posts/YYYY-MM-DD-title.md` |
| Donation page | `_pages/donate.md` |
| Navigation menu | `_data/navigation.yml` |
| This guide | `_pages/how-to-update.md` |
