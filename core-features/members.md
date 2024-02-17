# Memberships and Subscriptions

Bold supports both free and paid members. By default, users who sign up will automatically be free members and can sign in later with a magic link.

If you set up paid tiers, members who have previously registered for free can pay a subscription to access your website's premium content.

## Members Pages

Bold provides custom templates for Sign Up, Sign In, Newsletter, Membership and Account pages, below is a description of the purpose of each of these pages and the process of creating and enabling them.

### Sign Up

This page is where users can sign up on your site. If they are already free members then they will see the subscription plans you have in place and will be able to pay to become paid members.

[Live demo](https://bold.eduardogomez.io/signup/)

### Sign In

On this page members of your site will be able to sign in. The only thing they will need is their email address in order to receive a magic link with which to sign in.

[Live demo](https://bold.eduardogomez.io/signin/)

### Membership

If users visiting this page are not registered or are free members they will see the subscription plans you have in place and will be able to pay to become paid members.

[Live demo](https://bold.eduardogomez.io/membership/)

### Account

On this page members will be able to view their account details. If they are free members then they will also see a link to go to the page where the subscription plans are shown.

If they are paid members then they will see a list of their subscriptions, each with information such as price, expiration date, payment information and a link to cancel.

### Newsletter

On this page any user can enter their email address to receive in their inbox content from your site periodically.

[Live demo](https://bold.eduardogomez.io/newsletter/)

## Enabling Members Pages

The first thing you need to do to allow members on your site is to enable this feature in the Ghost Admin and connect a **Stripe** account. The [Ghost documentation](https://ghost.org/docs/members/requirements/) provides a comprehensive overview of the requirements and steps necessary to enable it correctly.

### Upload Routes File

Unzip the theme file (`bold.zip`) and upload the `routes.yaml` file in the Ghost Admin by heading to `Settings` --> `Labs` --> `Beta features` --> `Routes`

### Create Members Pages

You must now create the following pages in the Ghost Admin:

* Sign Up
* Sign In
* Membership
* Account
* Newsletter

To create each page please follow these steps:

1. In the Ghost Admin head to `Pages` and click on `New page`

2. Give it a title 

If you decide to use another title for each page it is important that you manually change the **Page URL** in the page settings so that the value **matches** its corresponding one in the table below, otherwise it will not work:

| Page       | URL             |
| ---------- | --------------- |
| Sign Up    | **/signup**     |
| Sign In    | **/signin**     |
| Membership | **/membership** |
| Account    | **/account**    |
| Newsletter | **/newsletter** |

3. If you want to change the text displayed below the title of the pages, you can add your own custom excerpt in the page settings

4. You can also add a **feature image** if you want (except for Membership and Account pages)

5. Publish the pages and you're done!

## Membership Tiers

Ghost allows you to offer multiple membership products, each with unique prices, benefits, and content access levels.

A tiered pricing strategy makes it possible to grow your business by offering different products and benefits to your audience.

If you want to know how to create and configure your own custom tiers you can check the [Ghost documentation](https://ghost.org/help/tiers/). Your tiers will be automatically displayed on the **Membership** page.

![](https://res.cloudinary.com/edev/image/upload/v1708186985/bold/CleanShot_2024-02-17_at_17.21.54.jpg)

## Portal

If you want to use [Portal](https://ghost.org/help/setting-up-portal/) for all Members functionalities instead of the ones provided by the theme you can enable the `Portal for membership experience` setting found in the [theme settings](/basics/theme-settings#portal-for-membership-experience) as shown in the following screenshot:

![](https://res.cloudinary.com/edev/image/upload/v1708187145/bold/CleanShot_2024-02-17_at_17.24.06.jpg)

By enabling this option all links and buttons for sign up, sign in, newsletter, account and other membership-related features will use the Portal interface instead of linking to the custom pages that the theme provides.

This also means that **if you want to use Portal you don't need to follow the steps described above** in the setup section as the theme will use the Portal interface itself that Ghost provides by default.

## Disable Members Features

If you don't want to use any of the Members features you can disable it in the Ghost Admin, to do so just head to `Settings` --> `Access`, in the `Subscription access` section you can choose who should be able to subscribe to your site, in this case you can choose that nobody will be able to subscribe or sign in.

![](https://res.cloudinary.com/edev/image/upload/v1705190409/ghost/CleanShot_2024-01-14_at_00.58.54.png)

When Members is disabled all the sign up and sign in buttons will be removed, also the newsletter form will be removed.
