# Helium Jekyll
## A new Bootstrap 4 theme

### Installation

Fork (do not clone) the project, `cd` into the project folder and run the following command:
```gem install github-pages```

This will install the github-pages gem and all dependencies (including jekyll).

Once you have made the desired changes on the forked version of this site, construct and test your site locally, by going into the project directory and type the following command in your terminal:

```jekyll build```

This will create (or modify) a `_site/` directory, containing everything from `assets/`, and then the `index.md` and all `pages/*.md` files, converted to html. (So there’ll be `_site/index.html` and the various `_site/pages/*.html`.)

Type the following in order to “serve” the site. This will first run build, and so it does not need to be preceded by jekyll build.

```jekyll serve --config _config-dev.yml```

To make jekyll automatically re-build your changes you can also add the --watch option:

 ```jekyll serve --watch```
    
Now open your browser and go to `http://localhost:4000`

For additional assistance, view this post: [https://heliumjk.github.io/lessons/2017/01/17/testing-locally-helium-jekyll](https://heliumjk.github.io/lessons/2017/01/17/testing-locally-helium-jekyll)

## Add images to post

All images must be stored under ```assets/images/``` directory

---

<a href="https://jekyll-themes.com">
    <img src="https://img.shields.io/badge/featured%20on-JT-red.svg" height="20" alt="Jekyll Themes Shield" >
</a>

Helium is a fast, modern and configurable [Jekyll](http://jekyllrb.com/) theme with some tricks up it's sleeve. It has a live theme switcher and it's main blog layout display prominent hero images for posts with colored overlays and nice animations.

![helium sample](https://raw.githubusercontent.com/heliumjk/heliumjk.github.io/master/assets/images/helium-screenshot.jpg)
![helium theme](https://raw.githubusercontent.com/heliumjk/heliumjk.github.io/master/assets/images/helium-screenshot1.jpg)

## Features
Though minimalistic-looking by nature, dactl is easily configurable and includes quite a lot of niceties:

Main features:
* [Bootstrap 4](https://v4-alpha.getbootstrap.com/)
* [Font Awesome](http://fontawesome.io/)
* 100+ UI Blocks
* Responsive design

Jekyll-specific features:
* Fully compatible with Jekyll 3.x and GitHub Pages
* SEO optimized
* [Google Analytics](https://www.google.com/analytics/) support
* [Google AdSense](https://www.google.com/adsense/start/) support
* [Disqus](https://disqus.com/) comments support

Other features:
* Blog page
* Landing page samples
* Tags functionality and tags pages
* Link posts functionality
* Mobile slider scrolling
* Emoji support ⚡️⚡️⚡️ by copy paste from [getemoji](http://getemoji.com/)

Some of the features listed above can be easily configured or disabled by you.

## Information about Helium
At it's core, dactl is a forked version of [sentenza](https://github.com/sentenza/jekyll-material-design) but it has been almost entirely rewritten from scratch.  
I have just started my journey in the world of web development, learning new things on the way.  
Looking for a way to put my newly acquired skills to test I found Jekyll and I quickly realized that it's going to be a good learning experience since I don't like building 'dummy' projects.  
I've built this theme as a way to develop my skills further.

You can find credits at the bottom of this Readme file.  
**All** feedback is welcome, both positive and negative.

## Installation
### Running locally
Assuming you've got Jekyll [installed](https://jekyllrb.com/docs/installation/), clone or download this repo, `cd` to wherever you've put `helium` folder and run `jekyll -s'`

### Hosting on GitHub
Fork this repo and rename it to `yourusername.github.io`... and edit the `_config.yaml` file whit your github address and your links (such as social media username, email, name, ecc.)!  
Your new helium-themed Jekyll blog should be up and running at yourusername.github.io.  


## Additional information about some features
### Hero images and blog layout
Liquid 'script' which is used to append correct hero image and overlay color as set in post YAML Front matter was written by me and while it's really basic it functions properly.  
You can read more about it and see the code in `include/utils/hero.html`.

#### Tags & Tags Pages
Tags and tag pages are supported by using Jekyll's native collections functionality.  

## Credits
### Resources used
- [Helium B4](https://uideck.com/products/helium-ui-kit/)
- [Font Awesome](http://fontawesome.io/)
- [Bootstrap 4](https://v4-alpha.getbootstrap.com/)

### Inspiration and thoughtful code-jacking
Inspiration and bits of things listed below are present inside dactl's code:
- [Daktilo](https://github.com/kronik3r/daktilo) - dactl is based on Daktilo and inherits it's one-column layout.
- [Hydejack](https://github.com/qwtel/hydejack/) - I've learned a lot about Jekyll when I took apart [@qwtel](https://github.com/qwtel/)'s excellent fork of [Hyde](https://github.com/poole/hyde) theme. I embraced his more partials = everything is easier to edit policy. Hydejack theme gave me an idea on how to create hero images liquid scripting, loading google fonts and using rem's/em's and more.
- [Minimal Mistakes](https://github.com/mmistakes/minimal-mistakes) - This guy makes awesome themes and writes a lot about Jekyll and it's more obscure use cases on his blog, [Made Mistakes](https://mademistakes.com). Looking through his theme's code - Minimal Mistakes in particular - gave me lot of information about how to build a robust theme and how to make it configurable within `_config.yml`
- [Trophy](https://github.com/thomasvaeth/trophy-jekyll) - Link border slide animation SASS mixin which I slightly modified to be able to easily change the direction of the animation.
- Various blog posts about Jekyll and [Stackoverflow](https://www.stackoverflow.com) posts with useful [Liquid](https://github.com/Shopify/liquid) snippets.

## License
All parts of helium Jekyll theme are free to use and abuse under the open-source [MIT license](http://opensource.org/licenses/mit-license.php).

## TO DO
- [ ] Add Ads Block to home page 
- [ ] Minimize `.css` in `<head>` and all images for faster load times
- [ ] 404 page styles
- [ ] Create hightlight style for code parts

## Help out
Im [Antonio Trento](https://antoniotrento.github.io) and I'm looking for funds to be able to open my IT development company with many on-site projects, unfortunately they are hardly feasible without collaboration and an economic base.

If you want to contribute you can donate ethereum or bitcoin:
- [Donate Bitcoins](https://blockchain.info/address/1B9rDoFCndbsKXL9QiefUcUGUbJH9Y1i6M)
- Donate Ethereum on this wallet 0x657d7b5d541c1c4a4E7F04EF3F0ECDa3c4299D8a
