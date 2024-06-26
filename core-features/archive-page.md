# Archive Page

On this page, visitors to your publication will be able to find a list with all the posts ordered chronologically and grouped by year. You can explore a live demo by clicking [this link](https://bold.eduardogomez.io/archive), and it looks like this:

![](https://res.cloudinary.com/edev/image/upload/v1710002292/bold/CleanShot_2024-03-09_at_17.37.12.jpg)

## Enable Archive Page

To enable this page please follow these steps:

1. Unzip the theme file (`bold.zip`) and upload the `routes.yaml` file in the Ghost Admin by heading to `Settings` --> `Labs` --> `Beta features` --> `Routes`

2. In the Ghost Admin head to `Pages` and click on `New page`

3. Give it a title (e.g. _Archive_)

::: warning
If you decide to use another title for this page it is important that you manually change the **Page URL** in the page settings so that the value is `archive`, otherwise it will not work.
:::

4. Publish the page and you're done!

::: tip
You do not need to add content to this page as it is automatically generated.
:::

### Using a different URL

If you want to use a different URL, `/timeline` for example, you can follow these steps:

1. Create a backup of the theme file (`bold.zip`)

2. Unzip the theme file

3. Open the file `routes.yaml` with a code editor

4. Replace `archive` with `timeline` as is shown in the highlighted lines in the following example:

```yaml
  /archive/:  // [!code --]
  /timeline/: // [!code ++]
    controller: channel
    template: archive
    data: page.archive  // [!code --]
    data: page.timeline // [!code ++]
```

::: warning
Please note that the `template` should keep the same value `archive`, otherwise it won't work.
:::

5. Save your changes

6. Head to the Ghost Admin and upload the file `routes.yaml` in `Settings` --> `Labs` --> `Beta features` --> `Routes`
