# Personal Readme

## CLI Commands Cheat Sheet

yarn start
starts the local server with hot-reloading

### Build for Deployment

yarn build
builds the static directory for publishing to the web.

### Publish using github pages

Edit website/siteConfig.js and add following stuff

"""
const siteConfig = {
  ...
  url: 'https://USERNAME.github.io', // Replace USERNAME with your GitHub username.
  baseUrl: '/docusaurus-tutorial/', // The name of your GitHub project.
  projectName: 'docusaurus-tutorial',  // The name of your GitHub project. Same as above.
  organizationName: 'USERNAME' // Your GitHub username.
  ...
}
"""

run yarn build.

GIT_USER=Zenahr CURRENT_BRANCH=master USE_SSH=true npm run publish-gh-pages

The hosted files can then be found under
"""
https://github.com/USERNAME/$projectName
"""

hosted page can be viewed via
https://Zenahr.github.io/$projectName

## Glossary


the markdown in /docs works as follows:

Header consists of an id, and title.
The id determines the link of the document eg id: intro ---> .../docs/intro.html
If you'd like to add a sidebar, you could also add zero or more elements to it in order for it to show up.
Remember to add any new docs to the sidebars.json file so that the linking works properly across different docs.
