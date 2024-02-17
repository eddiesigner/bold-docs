# Comments

Bold supports both native comments and third-party solutions. This guide describes how to enable both options.

## Native Comments

Native comments are disabled by default. If you want to use them in your publication, you must first enable them in `Settings` --> `Membership` --> `Access`, as shown in the following screenshot:

![](https://res.cloudinary.com/edev/image/upload/v1705165061/ghost/CleanShot_2024-01-13_at_17.55.55.png)

You can learn more about Comments in the [official documentation](https://ghost.org/help/commenting/).

## Third-party Comments

Bold is also compatible with third-party solutions, you can use any of the available [Ghost integrations](https://ghost.org/integrations/?tag=community), the installation is usually quite simple, below you can see an example of how to add **Disqus** and **Cove** comments to your publication. The setup process for other solutions is pretty much the same.

### Disqus

Bold integrates perfectly with [Disqus](https://disqus.com/), all you have to do is the following:

1. After creating an account in Disqus, you have to create a new site in the [admin](https://disqus.com/admin) of that platform

2. You must copy the **shortname** of your brand new site, this can be found in the preferences of your site

3. Create a backup of the theme file (`bold.zip`)

4. Unzip the theme file

5. Open the file `partials/comments.hbs` with a code editor and comment out the following lines of code:

```hbs
{{!-- // [!code ++]
  {{#if comments}}
    <section class="bo-comments">
      <div class="bo-generic-wrapper">
        <div class="bo-wrapper">
          <div class="bo-comments__wrapper js-comments">
            {{comments}}
          </div>
        </div>
      </div>
    </section>
  {{/if}}
--}} // [!code ++]
```

6. Remove the comments surrounding the following code block located at the end of the file:

```hbs
{{!--  // [!code --]
  <section class="bo-comments">
    <div class="bo-generic-wrapper">
      <div class="bo-wrapper">
        <div class="bo-comments__wrapper js-comments">
          <!-- Paste here the provided code snippet -->
        </div>
      </div>
    </div>
  </section>
--}}  // [!code --]
```

7. Paste the code provided by Disqus below `<!-- Paste here the provided code snippet -->` so that it looks somewhat like the following:

```hbs
<section class="bo-comments">
  <div class="bo-generic-wrapper">
    <div class="bo-wrapper">
      <div class="bo-comments__wrapper js-comments">
        <!-- Paste here the provided code snippet -->
        <div id="disqus_thread"></div>
        <script>
          var disqus_config = function () {
            this.page.url = "{{url absolute="true"}}";
            this.page.identifier = "ghost-{{comment_id}}"
          };
          (function () {
            var d = document, s = d.createElement('script');
            s.src = 'https://SHORT_NAME.disqus.com/embed.js'; // [!code highlight]
            s.setAttribute('data-timestamp', +new Date());
            (d.head || d.body).appendChild(s);
          })();
        </script>
      </div>
    </div>
  </div>
</section>
```

8. Replace `SHORT_NAME` with the **shortname** you got in step 2

8. Finally save the file, zip the theme folder and upload it again

### Cove

[Cove](https://cove.chat/) is an alternative comment platform that allows you to embed fully functional comment threads from your subscribed members, allowing you to build a community for your membership audience on Ghost. In other words, Cove lets subscribers of your content log in and comment on your content.

There is an [official guide](https://ghost.org/integrations/cove-comments/) on how to integrate Cove with Ghost, the only difference is step 4 (Add the code to your theme), the difference is that you have to replace all the content of `partials/comments.hbs` with the following block of code:

```hbs
{{#if @site.members_enabled}}
  <section class="bo-comments">
    <div class="bo-generic-wrapper">
      <div class="bo-wrapper">
        <div class="bo-comments__wrapper js-comments">
          <!-- Paste here the provided code snippet -->
          <h2><span id="cove-count"></span> Comments</h2>
          <div id="cove"></div>

          {{#if @member}}
            <p>Signed in as {{@member.email}} · <a href="javascript:" data-members-signout>Sign out</a></p>
          {{else}}
            <p>Become a {{@site.title}} member below to join the conversation. As a member, you will also receive new posts by email (you can unsubscribe at any time).</p>
            <form data-members-form="signin" id="cove-login">
            <input class="cove-input" data-members-email type="email" required="true" placeholder="your@email.com" />
            <button type="submit" class="cove-button">Sign in to comment</button>
            <span class="signin-success" style="display:none">Great! Please check your inbox for a log in link.</span>
            <span class="signin-error" style="display:none">Something didn't work. Please try again.</span>
            </form>
          {{/if}}

          <script>
          const Cove = {
            publication: "YOUR_SITE_ID",
            contentId: "{{id}}",
            memberId: "{{@member.uuid}}",
            memberEmail: "{{@member.email}}"
          }
          </script>
        </div>
      </div>
    </div>
  </section>
{{/if}}
```

Finally save the file, zip the theme folder and upload it again.

For more detailed info please refer to their [official documentation](https://cove.chat/help/install-cove-in-ghost/).
