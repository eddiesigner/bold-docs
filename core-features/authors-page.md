# Authors Page

This page is where you can see all the authors at a glance (you could use it as a Team page if you will), you can see a live demo in [this link](https://bold.eduardogomez.io/authors/), it looks like this:

![](https://res.cloudinary.com/edev/image/upload/v1708187849/bold/CleanShot_2024-02-17_at_17.36.15.jpg)

## Enable Authors Page

To enable this page please follow these steps:

1. In the Ghost Admin head to `Pages` and click on `New page`

2. Give it a title (e.g. _Authors_)

::: warning
If you decide to use another title for this page it is important that you manually change the **Page URL** in the page settings so that the value is `authors`, otherwise it will not work.
:::

3. Publish the page and you're done!

::: tip
You do not need to add content to this page as it is automatically generated.
:::

### Using a different URL

If you want to use a different URL, `/team` for example, you can follow these steps:

1. Create a backup of the theme file (`bold.zip`)

2. Unzip the theme file

3. Open the file `routes.yaml` with a code editor

4. Replace `authors` with `team` as is shown in the highlighted lines in the following example:

```yaml
  /authors/:  // [!code --]
  /team/: // [!code ++]
    template: authors
    data: page.authors  // [!code --]
    data: page.team // [!code ++]
```

::: warning
Please note that the `template` should keep the same value `authors`, otherwise it won't work.
:::

5. Save your changes

6. Head to the Ghost Admin and upload the file `routes.yaml` in `Settings` --> `Labs` --> `Beta features` --> `Routes`
