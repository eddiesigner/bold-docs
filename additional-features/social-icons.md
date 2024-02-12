# Social Icons

Below is a table with all the available icons and their respective IDs, which are used to select the desired icon. Later on, an example of how to use them is provided.

| Icon  |    ID    |
| -------- | --------------- |
| Amazon | `amazon` |
| Apple | `apple` |
| Apple Podcasts | `applepodcasts` |
| Behance | `behance` |
| Blogger | `blogger` |
| CodePen | `codepen` |
| DeviantArt | `deviantart` |
| Discord | `discord` |
| Dribbble | `dribbble` |
| Dropbox | `dropbox` |
| Facebook | `facebook` |
| Figma | `figma` |
| Flickr | `flickr` |
| GitHub | `github` |
| GitLab | `gitlab` |
| Google | `google` |
| Google Podcasts | `googlepodcasts` |
| Instagram | `instagram` |
| Kik | `kik` |
| Line | `line` |
| Linkedin | `linkedin` |
| Medium | `medium` |
| Messenger | `messenger` |
| Notion | `notion` |
| Overcast | `overcast` |
| PayPal | `paypal` |
| Pinterest | `pinterest` |
| Reddit | `reddit` |
| RSS | `rss` |
| Skype | `skype` |
| Slack | `slack` |
| Snapchat | `snapchat` |
| SoundCloud | `soundcloud` |
| Spotify | `spotify` |
| StackOverflow | `stackoverflow` |
| Stitcher | `stitcher` |
| Substack | `substack` |
| Telegram | `telegram` |
| TikTok | `tiktok` |
| Tumblr | `tumblr` |
| Twitch | `twitch` |
| Twitter | `twitter` |
| Vimeo | `vimeo` |
| Vk | `vk` |
| Wechat | `wechat` |
| Whatsapp | `whatsapp` |
| X | `x` |
| Yelp | `yelp` |
| YouTube | `youtube` |

Its usage is straightforward. For example, if you want to use the Instagram icon in any of the theme's templates, you can use the following code:

```hbs
{{> icon id="instagram" size="20"}}
```

As you can see, in addition to passing the icon's `id`, you can also define the icon's size in pixels using the `size` attribute.

If you want the icon to have a specific color, you can wrap it with a `<span>` element and assign the desired color to that element, either through a class or an inline style, as shown in the following example:

```hbs
<span style="color: #833ab4;">
  {{> icon id="instagram" size="20"}}
</span>
```
