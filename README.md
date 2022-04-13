# :warning::warning: Note: You probably don't want this branch! :warning::warning:

This branch is a **one-off feature branch** for a tailored version of the starter to be
included in the Next.JS examples repository. This branch should never be merged into master!

If you're looking to download the ButterCMS Next.JS starter
project, you'll want to head over to 
[https://github.com/ButterCMS/nextjs-starter-buttercms](https://github.com/ButterCMS/nextjs-starter-buttercms)
instead!

If you need to update our nextjs example inside the nextjs example repo, you will need to:
- pull changes from master INTO this branch, if needed. (Can rebase if necessary, but all
commits from this branch need to stay "on top.")
- make changes to this repo, merging branches into this feature branch as necessary, but
DO NOT MERGE THIS BRANCH INTO MASTER.
- It's important to note that next.js has stringent requirements for updates to the canary repo for these examples. Do NOT try to update the .gitignore. You can add or update sections of the readme, but do not delete sections. Do not pin a specific node version in the requirements. All packages and dependencies need to be updated to the latest version, with no warnings, or the PR will be rejected. Next.js requires the use of the `<Image />` tag, versus `<img>`; as such, the profile image for the various blog posts, etc. has been deleted to make updates easier/quicker.
- fork the next.js dev branch (canary) and checkout a branch on your fork, e.g., `UPDATE_BUTTERCMS_EXAMPLE`
- copy all of this repo's updated files into your canary dev branch in the `examples/cms-buttercms` folder,
replacing the content currently in there. Almost all of the files should stay the same!
- delete this little disclaimer at the top of the readme inside the `examples/cms-buttercms` folder
- Make sure linting passes by running `yarn lint` inside of the next.js repo. If linting
is not passing because of something outside of our starter project, you can try 
`yarn lint-no-typescript`. 
- Open a PR to merge your `UPDATE_BUTTERCMS_EXAMPLE` branch into the next.js canary repo.

# A fully-functional, drop-in proof-of-concept Next.js app using ButterCMS

This Next.js starter project fully integrates with dynamic sample content from your ButterCMS account, including main menu, pages, blog posts, categories, and tags, all with a beautiful, custom theme with already-implemented search functionality. All of the included sample content is automatically created in your account dashboard when you sign up for a free trial of ButterCMS.

A copy of this starter project can be easily and quickly deployed to Vercel with the click of a button.

This example showcases Next.js's [Static Generation](https://nextjs.org/docs/basic-features/pages) feature using [ButterCMS](https://buttercms.com/) as the data source.

## Demo

Check out our live demo: [https://nextjs-starter-buttercms.vercel.app/](https://nextjs-starter-buttercms.vercel.app/)

## Deploy your own

Once you have access to your Butter API token, you can deploy your Butterized proof-of-concept app to Vercel, the creators of Next.js, and spread your love of Butter. By clicking the button below, you'll create a copy of our starter project in your Git provider account, instantly deploy it, and institute a full content workflow connected to your ButterCMS account. Smooth.

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2FButterCMS%2Fnextjs-starter-buttercms&env=NEXT_PUBLIC_BUTTER_CMS_API_KEY&envDescription=Your%20ButterCMS%20API%20Token&envLink=https%3A%2F%2Fbuttercms.com%2Fsettings%2F&project-name=nextjs-starter-buttercms&repo-name=nextjs-starter-buttercms&redirect-url=https%3A%2F%2Fbuttercms.com%2Fonboarding%2Fvercel-starter-deploy-callback%2F&production-deploy-hook=Deploy%20Triggered%20from%20ButterCMS&demo-title=ButterCMS%20Next.js%20Starter&demo-description=Fully%20integrated%20with%20your%20ButterCMS%20account&demo-url=https%3A%2F%2Fnextjs-starter-buttercms.vercel.app%2F&demo-image=https://cdn.buttercms.com/r0tGK8xFRti2iRKBJ0eY&repository-name=nextjs-starter-buttercms)

### Related examples

- [WordPress](/examples/cms-wordpress)
- [DatoCMS](/examples/cms-datocms)
- [Sanity](/examples/cms-sanity)
- [TakeShape](/examples/cms-takeshape)
- [Prismic](/examples/cms-prismic)
- [Contentful](/examples/cms-contentful)
- [Agility CMS](/examples/cms-agilitycms)
- [Cosmic](/examples/cms-cosmic)
- [Strapi](/examples/cms-strapi)
- [Storyblok](/examples/cms-storyblok)
- [GraphCMS](/examples/cms-graphcms)
- [Kontent](/examples/cms-kontent)
- [Ghost](/examples/cms-ghost)
- [Umbraco Heartcore](/examples/cms-umbraco-heartcore)
- [Blog Starter](/examples/blog-starter)
- [Builder.io](/examples/cms-builder-io)

## How to use

### Option 1. Install via Github and NPM or Yarn

First, install the dependencies by cloning the repo and running one of the following commands, depending on your current setup:

```bash
git clone https://github.com/ButterCMS/nextjs-starter-buttercms.git
cd nextjs-starter-buttercms
npm install # or yarn install
``` 

### Option 2. Install via Create-Next-App

Execute [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app) with [npm](https://docs.npmjs.com/cli/init) or [Yarn](https://yarnpkg.com/lang/en/docs/cli/create/) to bootstrap the example:

```bash
npx create-next-app --example cms-buttercms cms-buttercms-app
# or
yarn create next-app --example cms-buttercms cms-buttercms-app
# or
pnpm create next-app -- --example cms-buttercms cms-buttercms-app
```

## Configuration

### Step 1. Create an account on ButterCMS

First, [create an account on ButterCMS](https://buttercms.com/).

After signing up, you’ll be presented with your free API token. We’ll use this in the next step.

### Step 2. Set up environment variables

Copy the `.env.local.example` file in this directory to `.env.local` (which will be ignored by Git):

```bash
cp .env.local.example .env.local
```

Then set each variable on `.env.local`:

- `BUTTERCMS_API_KEY` should be set as the API key.

### Step 3. Run Next.js in development mode

When you sign up to ButterCMS, it creates all of the example content used by this starter project. You can run Next.js in development mode to view your fully-functional starter project, including landing page with 
API-based components, API-based menu, and a blog.

```bash
npm install
npm run dev

# or

yarn install
yarn dev
```

Your starter project should be up and running on [http://localhost:3000](http://localhost:3000)! If it doesn't work, post on [GitHub discussions](https://github.com/vercel/next.js/discussions).

### Step 4. Try preview mode

Your starter project is automatically configured to show draft changes saved in your Butter account when run locally or deploy to a hosting provider. To disable this behavior, set the following value in your .env file: PREVIEW=false.

To try preview mode, [create a blog post](https://buttercms.com/post/):

- Set the **Title** as `Draft Post Test`.
- Fill the content and summary with dummy text.

Most importantly, **do not publish** the blog post. Instead, click **Save Draft**.

Now, if you go to the your blog list view page on localhost: [http://localhost:3000/#blog](http://localhost:3000/#blog), you won't see this post because it’s not published. However, if you use **Preview Mode** by deleting `PREVIEW=false` from your `.env.local` file will, your new post will appear ([Documentation](https://nextjs.org/docs/advanced-features/preview-mode)).


**Tip**: [You can set a preview URL on ButterCMS](https://buttercms.com/kb/preview-urls) for pages
deployed to Vercel, allowing you to preview changes from within your Butter account!. Sweet!

### Step 5. Deploy on Vercel

You can deploy this app to the cloud with [Vercel](https://vercel.com?utm_source=github&utm_medium=readme&utm_campaign=next-example) ([Documentation](https://nextjs.org/docs/deployment)).

#### Deploy from our template

If you want to deploy a copy of our starter to Vercel without any changes, you can just click this button:

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2FButterCMS%2Fnextjs-starter-buttercms&env=NEXT_PUBLIC_BUTTER_CMS_API_KEY&envDescription=Your%20ButterCMS%20API%20Token&envLink=https%3A%2F%2Fbuttercms.com%2Fsettings%2F&project-name=nextjs-starter-buttercms&repo-name=nextjs-starter-buttercms&redirect-url=https%3A%2F%2Fbuttercms.com%2Fonboarding%2Fvercel-starter-deploy-callback%2F&production-deploy-hook=Deploy%20Triggered%20from%20ButterCMS&demo-title=ButterCMS%20Next.js%20Starter&demo-description=Fully%20integrated%20with%20your%20ButterCMS%20account&demo-url=https%3A%2F%2Fnextjs-starter-buttercms.vercel.app%2F&demo-image=https://cdn.buttercms.com/r0tGK8xFRti2iRKBJ0eY&repository-name=nextjs-starter-buttercms)

#### Deploy your local project

To deploy your local project to Vercel (one in which you've made changes), push it to GitHub/GitLab/Bitbucket and [import to Vercel](https://vercel.com/new?utm_source=github&utm_medium=readme&utm_campaign=next-example).

**Important**: When you import your project on Vercel, make sure to click on **Environment Variables** and set them to match your `.env.local` file.
