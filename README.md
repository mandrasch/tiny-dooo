# Deprecated

See https://github.com/mandrasch/11ty-up-massively for a newer version of my experiment

<hr>

# tiny-DoOO
Tiny prototype for the "Domain of One's Own" concept (https://domain-of-ones-own.de/). Empower students / teachers to publish their own tiny html websites with simple page navigation on Github Pages.

The html5up.com theme "Phantom" was used as example, but you can use every HTML template you want with small additions.

Preview: https://mandrasch.github.io/tiny-dooo/

## Play with it

[![Open in Gitpod](open-in-gitpod.svg)](https://gitpod.io/#https://github.com/mandrasch/tiny-dooo)


## Create your own tiny website

There are multiple ways on how to edit this project in your browser. You could use https://replit.com/ oder https://gitpod.io/# . 
A german description with screenshots can be found here: 
https://matthias-andrasch.eu/blog/2021/web-ides-fuer-kleine-domain-of-ones-own-experimente/ (Alternatively you can use [Github Desktop](https://desktop.github.com) and an editor such as [Visual Studio Code](https://code.visualstudio.com/) to edit this project on your local laptop) 

1. Click on "Use template" button to create your own repository

2. Sign up on https://replit.com/

3. Connect your GitHub Account

4. Select your newly created repository from list

5. Hit "Run"

6. Open "version control" in sidebar, give replit.com editing permissions for the github repository

7. Commit changes you made to Github

8. Enable GitHub pages (Settings > Pages > Branch: main)

9. Have fun editing it in your browser!


## Link to content pages

1. Create your page in `pages/` as .html file

2. To load my-project.html, use

    ```
    <a href="#/pages/my-project.html`>My project link</a>
    ```
    
    or use the following for markdown pages:

    ```
    <a href="#/pages/my-project.md`>My project link</a>
    ```

## Transfer it to your own webspace

See https://github.com/SamKirkland/FTP-Deploy-Action on how to transfer the website automatically to your webspace with help of Github Actions feature.

<hr>

## For the nerds:

### Install for another theme

With some simple steps HTML themes can be converted to use with tiny-dooo.

1. Add `ttiny-dooo-main-content-area` class to main content area where content should be loaded dynamilly

2. Add tiny-dooo-scripts at the end of body

    ```
    <!-- tiny-dooo -->
	<script src="tiny-dooo/universal-router.min.js"></script>
	<script src="tiny-dooo/marked.min.js"></script>
	<script src="tiny-dooo/tiny-dooo.js"></script>
	<!-- eo tiny-dooo -->
    ```

3. Link pages with `#/pages/filename`, e.g. `#/pages/test1` to load `pages/test1.html`



### Tech stack

- I thought about using the static site generator eleventy, but there is no easy way of running node / npm run start in browser IDEs yet, therefore I dropped the idea of using nodejs
- Instead I used the method of docsifys Manual initialization (https://docsify.js.org/#/quickstart?id=manual-initialization) and hash based routing

### Local development

- npm install
- npm start

### TODOs

- Bug: Navigating with back button index.html - load original content / reload page
- a11y check / improvements
- provide meaningful demo content

## License

Open Source - MIT (Sharing is caring)
