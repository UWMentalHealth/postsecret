# UWaterloo EngSoc Post Secret Service Online

![Hugo Build](https://github.com/uwmentalhealth/postsecret/workflows/Hugo%20Build/badge.svg?branch=master&event=push)

Website homepage can be found at https://uwmentalhealth.github.io/postsecret/home/

## Content Management
- Content is located in the `content/photo` folder
- Each term has its own subfolder, containing an `index.md` file and the images
- When an image is added to this subfolder, it is automatically displayed on the website
- The information in the `index.md` file gives the additional desciptions to fill out parts of the homepage
- An example term with content can be found at `content/photo/example_term`

### Adding a secret
- Add the image of the secret to your term's folder
- In the same folder edit `index.md` and add a new post under the `resources:` header with the following template:
```
- src: <FILENAME>
  name: <TITLE>
  params:
    order: <ORDER_NUM>
    alt_text: <ALT_TEXT>
    warning: <WARNING>
    description: <DESCRIPTION>
    button_text: <BUTTON_TEXT>
    button_url: <BUTTON_URL>
```
- Fill in the following variables (if a variable is marked optional, the entire line can be deleted if not needed):
  - `FILENAME` - The exact name of the image file.
  - `TITLE` - The title of the image shown in the popup.
  - `ORDER_NUM` - The order in which to show the post. Posts are shown in descending order, so the most recent are shown first.
  - `ALT_TEXT` - A transcription of the image's text for accessibility purposes.
  - `WARNING` - (Optional) If this string is set, the preview of the image will be blurred and the warning text will be shown.
  - `DESCRIPTION` - (Optional) Additional text shown on the popup alongside the image.
  - `BUTTON_TEXT` - (Optional) Text for the button in the popup that can link to additional resources.
  - `BUTTON_URL` - (Optional) Url of the button in the popup.

### Starting a New Term
- Within the `/content/photo` directory, find the current term's folder
- Edit the `index.md` file's `draft` property to be True (this means the term's content will be hidden on the site)
- Create a new folder for the year (format `YEAR_TERM`, where term is Winter=1, Spring=2, Fall=3)
- Within that folder, add a new file called `index.md`, with the following template:
```
---
title: <TERM_NAME>
draft: False

resources:

---
```
- Fill in the following variables:
  - `TERM_NAME` - A descriptive name for the term, ex "Fall 202 Term"


## Development
The site uses Hugo with a custom theme to generate the static website from a simple content format.

### Setup
- install `hugo-extended` from https://gohugo.io/getting-started/installing/

### Tips
- To start the development server run `hugo server -w`
- Bootstrap styling is preferred, see the [Bootstrap Docs](https://getbootstrap.com/docs/4.0/getting-started/introduction/)
- Sass stylesheets are used in the theme. Sass is an extension of css that compiles down to css, see the [Sass Docs](https://sass-lang.com/documentation)

## Deploy
- The site deploys automatically whenever a new commit appears on `master`
- This is done with GitHub actions, and the build site is put onto the `gh-pages` branch
- This site is hosted using GitHub Pages (for free)
