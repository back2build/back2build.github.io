---
layout: single
title: "How to Update This Site"
permalink: /how-to-update/
sidebar:
  nav: "how-to-update"
---

This guide walks you through how to make changes to the Back2Build website. Everything is done through GitHub's website — no software to install, no coding experience needed.

- **The website:** [https://back2build.github.io/](https://back2build.github.io/)
- **The files (GitHub):** [https://github.com/back2build/back2build.github.io](https://github.com/back2build/back2build.github.io)

### Jump to a common task

[Edit a Page](#editing-an-existing-page){: .btn .btn--info} [Edit a Student](#editing-a-student-profile){: .btn .btn--info} [Add a Student](#adding-a-new-student){: .btn .btn--primary} [Add a Blog Post](#adding-a-blog-post){: .btn .btn--success}

---

## Before You Start

**What you need:** A GitHub account and a web browser. If you don't have a GitHub account yet, create one for free at [github.com](https://github.com/signup). Once you have an account, ask Simba to add you to the [Back2Build organization](https://github.com/orgs/back2build/people) — you won't be able to make edits until you've been added.
{: .notice--info}

The website files live on GitHub. To make changes:

1. Go to [the repository on GitHub](https://github.com/back2build/back2build.github.io).
2. Sign in to your GitHub account (you must be a member of the [Back2Build org](https://github.com/orgs/back2build/people) to make edits).
3. Navigate to the file you want to change.
4. Make your edits and **commit** (save) them.

<div class="notice--success" markdown="1">
**"Commit" just means "save."** When GitHub asks you to "commit changes," it is asking you to save your work. Type a short note describing what you changed (e.g., "Update donate page") and click the green button.
</div>

<div class="notice--danger" markdown="1">
**Do not edit `_config.yml`, `_layouts/`, `_includes/`, or `_sass/`.** These control the site's structure and design. Everything you need to update is in `_pages/`, `_students/`, `_posts/`, and `_data/`.
</div>

## Editing an Existing Page

This is the simplest and most common task.

1. Navigate to the file you want to edit (use the links in the table below).
2. Click the **pencil icon** (top-right of the file content) to enter edit mode.
3. Make your changes. The text uses Markdown formatting — see the [Writing with Markdown](#writing-with-markdown) section if you need help.
4. Click **"Commit changes"**, add a short description of what you changed, and save.

### Which file is which page?

| Page on the website | File to edit |
|---|---|
| Homepage | [`_pages/home.md`](https://github.com/back2build/back2build.github.io/blob/main/_pages/home.md) |
| Donation page | [`_pages/donate.md`](https://github.com/back2build/back2build.github.io/blob/main/_pages/donate.md) |
| Students grid page (the heading text) | [`_pages/student-listing.md`](https://github.com/back2build/back2build.github.io/blob/main/_pages/student-listing.md) |
| Blog listing page | [`_pages/post-listing.md`](https://github.com/back2build/back2build.github.io/blob/main/_pages/post-listing.md) |

## Editing a Student Profile

[Open the _students folder](https://github.com/back2build/back2build.github.io/tree/main/_students){: .btn .btn--primary}

1. Click on the student's file (e.g., `nomaqhawe_ncube.md`).
2. Click the **pencil icon** to edit.
3. To change their **bio**, edit the text below the second `---` line.
4. To change their **details** (school, skills, photo), edit the fields in the top section between the two `---` lines.
5. Commit your changes.

Here's an example — to update a student's school from "Mpompoma L6" to "Mpompoma U6", change this line:

```yaml
excerpt: "Mpompoma L6"
```

to:

```yaml
excerpt: "Mpompoma U6"
```

**Be careful not to remove the colons or change the spacing in the top section.**
{: .notice--warning}

## Adding a New Student

This has two parts: uploading a photo, then creating the student's page.

### Step 1: Upload the student's photo

[Open the student photos folder](https://github.com/back2build/back2build.github.io/tree/main/assets/images/students){: .btn .btn--primary}

1. Click **"Add file"** then **"Upload files."**
2. Drag the photo in or click to browse your computer.
3. Click **"Commit changes."**

<div class="notice--warning" markdown="1">
**Photo tips:**
- Name the file something simple like `jane_headshot.jpg` (lowercase, no spaces).
- Crop to roughly square if possible.
- Keep the file size under 500 KB. If the photo is from a phone camera, it may be too large — use a free online tool to resize it first.
</div>

Remember the exact filename you used — you will need it in the next step.

### Step 2: Create the student file

[Open the _students folder](https://github.com/back2build/back2build.github.io/tree/main/_students){: .btn .btn--primary}

1. Click **"Add file"** then **"Create new file."**
2. In the filename box at the top, type the student's name in this format: `firstname_lastname.md`
   - All lowercase, underscore between names, must end in `.md`
   - Example: `jane_moyo.md`
3. Copy the template below and paste it into the file:

```yaml
---
title: "STUDENT FULL NAME"
excerpt: "SCHOOL and FORM/LEVEL"
header:
  teaser: /assets/images/students/PHOTO_FILENAME.jpg
sidebar:
  - title: "Focus Area"
    text: "THEIR MAIN FIELD"
  - title: "Skills"
    text: "SKILL 1, SKILL 2, SKILL 3"
---

Write the student's bio here.
```

{:start="4"}
4. Replace all the UPPERCASE PLACEHOLDER text with the student's real information.
5. Click **"Commit changes"**, type a short description like "Add student Jane Moyo", and click the green **"Commit changes"** button.

The photo you uploaded in Step 1 will automatically appear on both the Students grid page and the student's profile page.
{: .notice--success}

Here's what a filled-in example looks like:

```yaml
---
title: "Jane Moyo"
excerpt: "Mpompoma L6"
header:
  teaser: /assets/images/students/jane_headshot.jpg
sidebar:
  - title: "Focus Area"
    text: "Public Health"
  - title: "Skills"
    text: "Data Analysis, Community Health, Statistics"
---

Jane Moyo is a L6 student at Mpompoma High School in Bulawayo.
She is passionate about public health and hopes to study medicine.
```

### What each field does

| Field | What it controls |
|---|---|
| `title` | The student's name displayed as the page heading |
| `excerpt` | Short subtitle shown under their name on the Students grid |
| `header: teaser` | The student's photo (used on both the grid and profile page) |
| `sidebar: "Focus Area"` | Their main field of study or work |
| `sidebar: "Skills"` | Their specific skills, separated by commas |
| The text below the `---` | Their full bio, written in plain English |

## Updating a Student's Photo

1. Upload the new photo to the [`assets/images/students/`](https://github.com/back2build/back2build.github.io/tree/main/assets/images/students) folder (same process as [Step 1 above](#step-1-upload-the-students-photo)).
2. Edit the student's file in the [`_students/`](https://github.com/back2build/back2build.github.io/tree/main/_students) folder.
3. Update the photo filename in the `header: teaser` line. It only appears once — change it and you're done.

For example, to change from `jane_headshot.jpg` to `jane_new_photo.jpg`:

```yaml
header:
  teaser: /assets/images/students/jane_new_photo.jpg
```

## Removing a Student

[Open the _students folder](https://github.com/back2build/back2build.github.io/tree/main/_students){: .btn .btn--primary}

1. Click on the student's file.
2. Click the **"..."** menu (top-right of the file content).
3. Click **"Delete file."**
4. Commit the change.

This removes their profile page from the site. Their photo will still be in the images folder but won't be visible anywhere.
{: .notice--info}

## Adding a Blog Post

[Open the _posts folder](https://github.com/back2build/back2build.github.io/tree/main/_posts){: .btn .btn--primary}

1. Click **"Add file"** then **"Create new file."**
2. Name the file using this exact format: **`YYYY-MM-DD-short-title.md`**
   - The date must be real and in year-month-day format
   - Use hyphens between words in the title part
   - Example: `2026-04-06-fundraiser-recap.md`

**If the date format is wrong, the post will not appear on the site.**
{: .notice--danger}

{:start="3"}
3. Copy this template and paste it in:

```yaml
---
title: "YOUR POST TITLE"
categories:
  - News
tags:
  - event
---

Write your post content here.
```

`categories` and `tags` are optional but help organize posts. Common ones might be "News", "Events", or "Updates".

Here's a filled-in example:

```yaml
---
title: "Fundraiser Recap: April 2026"
categories:
  - News
tags:
  - fundraiser
---

We held our annual fundraiser on April 5th and raised $2,000
for student scholarships. Thank you to everyone who attended!

## Highlights

- 50 guests attended
- **$2,000** raised for scholarships
- Three new sponsors signed on
```

### Adding images to a blog post

To include an image in a post, first upload it to the [`assets/images/`](https://github.com/back2build/back2build.github.io/tree/main/assets/images) folder, then reference it in your post like this:

```markdown
![Description of the image](/assets/images/your-image-filename.jpg)
```

For example:

```markdown
![Group photo from the fundraiser](/assets/images/fundraiser-april-2026.jpg)
```

## Editing the Navigation Menu

The menu at the top of the site is controlled by one file: [**`_data/navigation.yml`**](https://github.com/back2build/back2build.github.io/blob/main/_data/navigation.yml)

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

For example, to add an "About" page to the menu, you would add these two lines at the end:

```yaml
  - title: "About"
    url: /about/
```

**Indentation matters** — use exactly 2 spaces before the dash, and 4 spaces before `title:` and `url:`. Do not use tabs.
{: .notice--warning}

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

### Images

```
![description of the image](/assets/images/filename.jpg)
```

Upload the image to the [`assets/images/`](https://github.com/back2build/back2build.github.io/tree/main/assets/images) folder first, then reference it with the path above.

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

<div class="notice--success" markdown="1">
**After saving:**
1. Wait about 1-2 minutes.
2. Go to [https://back2build.github.io/](https://back2build.github.io/) and **refresh the page** (Ctrl+R on Windows, Cmd+R on Mac).
3. You should see your changes.
</div>

If changes still don't appear after 5-10 minutes, something may have gone wrong — see Troubleshooting below.

## Troubleshooting

**My changes aren't showing up**
{: .notice--warning}

- Wait at least 2 minutes and refresh the page. GitHub Pages takes time to rebuild.
- If it has been more than 10 minutes, go to the [**"Actions"** tab](https://github.com/back2build/back2build.github.io/actions) in GitHub to check for build errors (a red X means something went wrong).

**A student photo is not showing**
{: .notice--warning}

- Double-check that the filename in the student file matches the actual photo filename exactly, including capitalization. `Jane_Headshot.jpg` is not the same as `jane_headshot.jpg`.
- Make sure the path starts with `/assets/images/students/`.

<div class="notice--danger" markdown="1">
**The page looks broken or blank**

The section between the two `---` lines at the top (called "front matter") is very strict about formatting:
- Always use **straight quotes** (`"like this"`), not curly/smart quotes. If you type in a word processor and paste, the quotes may be wrong.
- Always put a **space after every colon**. Write `title: "Hello"` not `title:"Hello"`.
- Do not add or remove spaces at the start of lines in the front matter — the indentation must stay exactly as it is in the template.
</div>

**A new blog post isn't appearing**
{: .notice--warning}

- The filename must start with a date in `YYYY-MM-DD-` format. Example: `2026-04-06-my-post.md`. If the date is missing or in the wrong format, Jekyll will ignore the file.

## Quick Reference

| What you want to change | Where to find it |
|---|---|
| Homepage content | [`_pages/home.md`](https://github.com/back2build/back2build.github.io/blob/main/_pages/home.md) |
| Student profiles | [`_students/`](https://github.com/back2build/back2build.github.io/tree/main/_students) |
| Student photos | [`assets/images/students/`](https://github.com/back2build/back2build.github.io/tree/main/assets/images/students) |
| Student template | [`_students/_TEMPLATE.md`](https://github.com/back2build/back2build.github.io/blob/main/_students/_TEMPLATE.md) |
| Blog posts | [`_posts/`](https://github.com/back2build/back2build.github.io/tree/main/_posts) |
| Donation page | [`_pages/donate.md`](https://github.com/back2build/back2build.github.io/blob/main/_pages/donate.md) |
| Navigation menu | [`_data/navigation.yml`](https://github.com/back2build/back2build.github.io/blob/main/_data/navigation.yml) |
| This guide | [`_pages/how-to-update.md`](https://github.com/back2build/back2build.github.io/blob/main/_pages/how-to-update.md) |
