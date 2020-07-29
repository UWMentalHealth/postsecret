# UWaterloo EngSoc Post Secret Service Online

![Hugo Build](https://github.com/uwmentalhealth/postsecret/workflows/Hugo%20Build/badge.svg?branch=master&event=push)

Website homepage can be found at https://uwmentalhealth.github.io/postsecret/home/

## Adding content
TODO
- To have new posts appear at the top of the page, use negative numbers for the order values.

## Development
The site uses Hugo with a custom theme to generate the static website from a simple content format.

### Setup
- install `hugo-extended` from https://gohugo.io/getting-started/installing/

### Tips
- To start the development server run `hugo server -w`
- Bootstrap styling is preferred, see the [Bootstrap Docs](https://getbootstrap.com/docs/4.0/getting-started/introduction/)
- Sass stylesheets are used in the theme. Sass is an extension of css that compiles down to css, see the [Sass Docs](https://sass-lang.com/documentation)

## Deploy
- The site deploys automatically whenever a new commit appears on master
- Github deploy actions will automatically run when PRs are merged to master

