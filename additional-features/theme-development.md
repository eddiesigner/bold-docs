# Theme Development

If you have knowledge in web development and want to make deeper changes in the theme or if you want to create a theme based on Bold you can follow this guide to learn how to setup a development environment easily.

## Development Mode

The following steps will guide you so that you can have a development environment on your machine without having to install Ghost locally:

1. Install [Docker](https://docs.docker.com/get-docker/) and [docker-compose](https://docs.docker.com/compose/install/)

2. Install [Nodejs](https://nodejs.org/en/download/) and [npm](https://www.npmjs.com/get-npm)

3. Create a backup of the theme file (`bold.zip`)

4. Unzip the theme file

5. Open a terminal and change to the `bold/src` directory

6. Run `npm install`

::: warning
Please ignore the following error if it appears after running `npm install`:
```
fatal: not a git repository (or any of the parent directories): .git
husky > Failed to install
```
:::

7. Run `npm run get-database` to get the Ghost database dump

8. From Ghost 4 onwards you need to pass your Stripe Webhook Secret as an environment variable which you can get from the [Webhooks page](https://dashboard.stripe.com/webhooks) in your dashboard

9. Open the file `src/docker-compose.yml` with a text/code editor and search for the following piece of code:

```
WEBHOOK_SECRET:
```

10. Copy the **Signing Secret** from your Stripe Webhook and paste it in that line of code, it should look something like this:

```
WEBHOOK_SECRET: whsec_xxxxxxxxxxxxxxxxxxxxxxx
```

11. Save your changes

For more information on how to set up your Stripe account please check out [this link](https://ghost.org/help/setup-members/)

12. Start Docker

13. Run `npm run docker-watch`

::: info
You will probably need to wait a little bit, even if a browser tab is opened, please keep waiting since the whole image and database will be created from scratch, probably it would take a few minutes, this will happen only the first time, the next time it should be faster.
:::

If everything goes well you should see this page in your browser:

![](https://user-images.githubusercontent.com/1477503/185713373-bd05eb67-cb19-4f8d-b65b-877aab3471f5.png)

After you enter your own credentials you still need to activate the theme in the Ghost Admin: `Settings` --> `Design and branding` --> `Change theme` --> `Installed themes`

![](https://res.cloudinary.com/edev/image/upload/v1708186120/bold/CleanShot_2024-02-17_at_17.06.29.jpg)

You only need to do this once, the next time you run the command everything should be ready automatically.

Now you should have an instant development setup and when you make changes you will see them right into the browser (hot-reloading).

You can see your blog in the following URL: `http://localhost:3000`

To access the Ghost Admin just enter this URL in your browser: `http://localhost:3000/ghost`

::: tip
If after a few seconds the page does not load, please wait a little longer or refresh the page several times, it will load ;)
:::

## Production Mode

When you are done making all your changes you can run `npm run production` (within the `src` directory) to build your theme in production mode.

`npm run production` will concatenate, minify, optimize and compress all your files and finally will generate the file `bold.zip` in the root of the theme folder.

Now you can upload this file in the Ghost Admin and you're ready to go!
