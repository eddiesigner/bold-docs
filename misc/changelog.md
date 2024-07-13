# Changelog

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
