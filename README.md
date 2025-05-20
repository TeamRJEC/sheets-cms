# Sheets-cms

This repo connects Google Sheet data to an Astro website using [opensheet](https://github.com/benborgers/opensheet).

To get started, clone fork or download this repo and run `npm install` in the directory to install dependencies.

To build the project run locally `npm run dev` and open [localhost:4321](http://localhost:4321) in your browser.

For further info and documentation on Astro, check out the [Astro docs](https://docs.astro.build/).

## Finding the sheet id

The sheet ID is the long string of characters in the URL of your Google Sheet.

![sheets-id](./public/id.png "sheets-id")

## Note: You need headers

Note that you will need headers in your sheet for the data to render properly. Drag the first row down to the second row to create headers.

![sheets-header](./public/header.png "sheets-header")

## 📝 Editing content

The content on the index page is rendered via the `src/Sheets.astro` component. Edit the `response` URL like so:

```astro
"https://opensheet.elk.sh/[GOOGLESHEET-ID-HERE]/1"
```

## Deployment

1. Sign in to [Cloudflare Pages](https://pages.cloudflare.com/) and create a new project.
2. Connect your GitHub account and authorize access to this repository.
3. Select **sheets-cms** as the project repository.
4. Use the default build command `npm run build` and set the build output directory to `dist`.
5. Save the configuration to trigger the initial build and deployment.

### Running the GitHub Actions workflow

A GitHub Actions workflow builds the site whenever you push to the main branch. To run it manually, open the **Actions** tab on GitHub and choose **Run workflow**.

### Environment variables

If your project requires environment variables, add them under **Project Settings → Environment Variables** in Cloudflare Pages. They will be available during the build step executed by GitHub Actions.

