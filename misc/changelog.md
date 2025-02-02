# Changelog

## v1.3.0

> Released on 03/02/2025

* Added support for [custom fonts](/basics/theme-settings.html#custom-fonts)
* Fixed a bug where the banner title displayed on posts where you don't have access could not be translated
* Fixed an issue where the price of a subscription plan had a wrong format under certain circumstances
* Fixed a bug where the logo image width could stretch too far on mobile devices
* Fixed a bug in membership tier cards where the checkmark icons could become smaller if the text was longer
* Reduced excessive spacing between the title and posts in the recommended posts section on a post page
* Updated Docker image (development only)
* Bump version number

````
Modified files:

* default.hbs
* members/account.hbs
* package.json
* partials/post-paywall.hbs
* src/docker-compose.yml
* src/sass/common/_global.scss
* src/sass/components/account/_account-subscription.scss
* src/sass/components/archive/_archive-entry.scss
* src/sass/components/general/_forms.scss
* src/sass/components/general/_logo.scss
* src/sass/components/membership/_plan-switcher.scss
* src/sass/components/membership/_tier.scss
* src/sass/components/post/_post-author.scss
* src/sass/components/post/_post-content.scss
* src/sass/components/post/_related-posts.scss
* src/sass/components/post/_section-title.scss
````

## v1.2.0

> Released on 25/11/2024

- It is now possible to display custom content on the [Membership page](https://bold.eduardogomez.io/membership/), to do so simply add content to the page directly in the Ghost Editor and this will be then displayed below the plan tiers (useful for FAQs, promotions, etc.)
- The signup, login and newsletter pages display the title and description defined in Ghost Admin if available, otherwise they display the current text provided by the theme
- Yearly plans are now displayed by default on the Membership page
- Members are now redirected to the Membership page after confirming their registration via the Sign Up page
- Paid members are now redirected to the Home page page after confirming their registration via the Sign Up page
- Added a button on the Account page so members can edit their account details
- The Announcement bar now displays at the top of the page instead of below the navigation bar, and fixed an issue where the bar would display in the wrong position under certain circumstances
- Added Threads icon
- Fixed an issue where success and error messages were not displayed after confirming via email under certain circumstances
- Fixed an issue where the wrong icon was displayed for the logout button
- Fixed an issue where the currency symbol and plan were not displayed in the free tier of the Membership page
- Fixed an issue where some submenu text would wrap to a second line
- Updated Docker image (development only)
- Bump version number

````
New files:

+ src/sass/components/membership/_membership-content.scss

Modified files:

*  assets/images/icons.svg
*  default.hbs
*  locales/en.json
*  locales/es.json
*  members/account.hbs
*  members/membership.hbs
*  members/newsletter.hbs
*  members/signin.hbs
*  members/signup.hbs
*  package.json
*  partials/header.hbs
*  src/docker-compose.yml
*  src/js/app.js
*  src/sass/common/_global.scss
*  src/sass/components/account/_account-header.scss
*  src/sass/components/auth/_auth-form.scss
*  src/sass/components/header/_announcement-bar.scss
*  src/sass/components/header/_mobile-menu.scss
*  src/sass/components/header/_submenu.scss
*  src/sass/components/membership/_membership-content.scss
*  src/sass/membership.scss
*  tags.hbs
````


## v1.1.0

> Released on 15/07/2024

* Fixed an issue where the signup, signin and newsletter pages didn't redirect to the home page after authenticating the user
* Fixed an issue where the close button in announcement bar had a wrong position
* Fixed an issue where there was no space between featured post cards when they were together
* Caption text in content cards is now centered
* Updated Docker image (development only)

````
New files:

+ .github/workflows/deploy-theme.yml
+ src/.env.example
+ src/.gitignore
+ src/deploy/index.js

Modified files:

* members/newsletter.hbs
* members/signin.hbs
* members/signup.hbs
* package.json
* src/docker-compose.yml
* src/package-lock.json
* src/package.json
* src/sass/components/general/_post-card.scss
* src/sass/components/header/_announcement-bar.scss
* src/sass/components/post/_post-content.scss
````

## v1.0.1

> Released on 15/04/2024

* Fixed an issue with size of auth image where image had a portrait aspect ratio
* Fixed an issue with figcaption in gallery card where font size was too big
* Fixed an issue with signup cards on mobile devices where vertical padding was too small when the card was the first element in the page
* Added max-width to signup cards content using split layout

````
Modified files:

* package.json
* README.md
* src/sass/components/auth/_auth.scss
* src/sass/components/post/_post-content.scss
````

## v1.0.0

* First release 🎉
