Fork
===========

Minor fork of [hugo-theme-one](https://github.com/resugary/hugo-theme-one) for personal use.

Change list:
* Increased spacing and added bar between navigation links for clarity
* Replaced highlight.js (run-time syntax highlighting) with [default Hugo highlighter 'Chroma'](https://gohugo.io/content-management/syntax-highlighting/) (compile-time).  
  One less resource to download, less JS to run. Google PageSpeed found highlight.js hindered page speed.
* Added 404 page.
* Added dynamic copyright year footer.
* Un-hidden post date at bottom of single posts

Problems left:
* No taxonomy (tags/categories) pages, despite styling in place to include them.
* Not very clear that the site-name link is the posts page.
* On small devices, with many header links, there is collision.
* No site map.
* The menu bar parameters are not passed in correctly.
* The whole single/list structure seems incorrect. May be wrong about this
* Remove webfonts?
* Perform all recommended Google PageSpeed optimisations
* Better support for social links?

Original readme below:


One
===========

[One](https://github.com/resugary/hugo-theme-one) is a minimal blog theme for Hugo, which is forked from [onetwothree](https://github.com/schollz/onetwothree). A demo is available [here](https://resugary.github.io/hugo-theme-one).

![Screenshot](https://github.com/resugary/hugo-theme-one/blob/master/images/screenshot.png)

It provides some new features and simplifications from original onetwothree. I tried to keep it minimal with less configuration to write a blog rather than play with a theme instead.

Features:  
- Add archives support for all posts in a single page  
- Homepage displayed with 7 latest posts default  
- Sytax highlighting support with ~~`highlight.js`~~ GO's [Chroma](https://github.com/alecthomas/chroma) (see fork details at top of readme)
- Google Analytics support  
- Full-text RSS support

## Installation

Clone this repository to your hugo theme directory.

```
git clone https://github.com/resugary/hugo-theme-one.git themes/one
hugo server -t=one
```

## Create New Posts

Posts should generally go under a `content/posts` directory, you may start like this:

```
hugo new posts/hello.md
```

## Create a fixed Page

Fixed pages such as an About page should be present at the root of the `content` directory:

```
hugo new about.md
```

To enable Archives, you should create a new file called `archives.md`:

```
hugo new archives.md

# then add the following line in the front matter
type: "archives"
```

## Configuration

Copy the `config.toml` in the root director of your hugo site. 

```toml
baseURL = "https://example.com"
languageCode = "en-us"
title = "My Hugo Site"

theme = "one"
googleAnalytics = "UA-123-45"

[params]
    navigation = ["archives.md", "about.md"]

```

Feel free to change the strings in this theme.

## License

Licensed under the MIT License.
