# Theme Appearance

Bold has three appearance themes: **Auto theme** (default), **Light theme** and **Dark theme**. Users can set their preferred theme from the dropdown that is available in the header of the page.

![](https://res.cloudinary.com/edev/image/upload/v1708185486/bold/CleanShot_2024-02-17_at_16.20.44.jpg)

## Auto Theme

The auto theme is selected by default, it adapts automatically according to the user's operating system preferences.

## Light Theme

The Light theme is activated either when the user explicitly chooses it from the menu or when the Auto theme is enabled and the user's operating system is set to light theme. If the user manually selects this theme from the menu, it will persist irrespective of the operating system theme, unless the user chooses a different theme.

As a reference, below are the colors defined in the Light theme in case you want to adapt them according to your preferences:

```css
:root {
  --accent: #E04F1B;
  --background: #F1F2ED;
  --body: #3A424E;
  --border: #DFE0DB;
  --featured: #FFFFFF;
  --card: #FFFFFF;
  --foreground: #15171A;
  --light-text: #575655;
  --text-on-accent: #FFFFFF;
  --highlighted: #FEE440;
  --focus: #90CDF4;
  --success: #1B8542;
  --error: #B91C1C;
  --translucent: rgba(241, 242, 237, 0.5);
}
```


If you want to change any of these colors, you can do so directly in the Ghost Admin by injecting your own styles in `Settings` --> `Code injection` --> `Site Header`. For example, if you want to change the background color you can inject the following code:

```html
<style>
  :root {
    --background: #F5F3EE;
    --translucent: rgba(245, 243, 238, 0.50);
  }
</style>
```

## Dark Theme

The Dark theme is activated either when the user explicitly chooses it from the menu or when the Auto theme is enabled and the user's operating system is set to dark theme. If the user manually selects this theme from the menu, it will persist irrespective of the operating system theme, unless the user chooses a different theme.

As a reference, below are the colors defined in the Dark theme in case you want to adapt them according to your preferences:

```css
[theme-mode="dark"] {
  --accent: #E04F1B;
  --background: #121212;
  --body: #D1D6DB;
  --border: #2D2C2C;
  --featured: #242424;
  --card: #1D1D1D;
  --foreground: #E8E8E8;
  --light-text: #89898A;
  --text-on-accent: #FFFFFF;
  --highlighted: #FEE440;
  --focus: #90CDF4;
  --success: #16A34A;
  --error: #E64141;
  --translucent: rgba(18, 18, 18, 0.5);
}
```

If you want to change any of these colors, you can do so directly in the Ghost Admin by injecting your own styles in `Settings` --> `Code injection` --> `Site Header`. For example, if you want to change the body text color you can inject the following code:

```html
<style>
  [theme-mode="dark"] {
    --body: #8DA5CE;
  }
</style>
```

::: info
If you want to change the **accent color**, it's better to do it in the `Design and branding` section of the Ghost Admin, as that value takes precedence over the one defined in these styles.
:::
