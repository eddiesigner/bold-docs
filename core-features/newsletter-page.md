# Newsletter Page

On this page any user can enter their email address to receive in their inbox content from your site periodically, you can see a live demo in [this link](https://bold.eduardogomez.io/newsletter/), it looks like this:

![](https://res.cloudinary.com/edev/image/upload/v1708187519/bold/CleanShot_2024-02-17_at_17.30.30.jpg)

## Enable Newsletter Page

To enable this page please follow these steps:

1. In the Ghost Admin head to `Pages` and click on `New page`

2. Give it a title (e.g. _Newsletter_)

::: warning
If you decide to use another title for this page it is important that you manually change the **Page URL** in the page settings so that the value is `newsletter`, otherwise it will not work.
:::

3. You can also add a **feature image** if you want

4. Publish the page and you're done!

::: tip
You do not need to add content to this page as it is automatically generated.
:::

### Using a different URL

If you want to use a different URL, `/subscribe` for example, you can follow these steps:

1. Create a backup of the theme file (`bold.zip`)

2. Unzip the theme file

3. Open the file `routes.yaml` with a code editor

4. Replace `newsletter` with `subscribe` as is shown in the highlighted lines in the following example:

```yaml
  /newsletter/:  // [!code --]
  /subscribe/: // [!code ++]
    template: members/newsletter
    data: page.newsletter  // [!code --]
    data: page.subscribe // [!code ++]
```

::: warning
Please note that the `template` should keep the same value `members/newsletter`, otherwise it won't work.
:::

5. Save your changes

6. Head to the Ghost Admin and upload the file `routes.yaml` in `Settings` --> `Labs` --> `Beta features` --> `Routes`
