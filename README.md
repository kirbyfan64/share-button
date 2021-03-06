<h1 align="center">Better Share Button</h1>

<p align="center">
  <img src="https://cldup.com/K3-R0bY2T8.gif"/>
</p>
<p align="center">
  <!--<a title="Build Status" href="https://travis-ci.org/carrot/share-button">
    <img src="http://img.shields.io/travis/carrot/share-button.svg?style=flat-square"/>
  </a>-->
</p>

Simple, light, flexible, and good-looking share button. [See it in action!](http://refi64.com/better-share-button)

This is a fork of
[the original Carrot share-button](https://github.com/carrot/share-button).
Because, after a year of being unmaintained, *it still looks freaking awesome*.

# An Introduction

## Why Should You Use This?
All major social networks have their own share widgets you can put on your page, but this isn't ideal for a variety of reasons:

1. They tend to be slow-loading.
2. They inject extra javascript and DOM elements into your page making it slower.
3. They generally aren't customizable enough to fit the design of your site.
4. Managing each provider's code snippets etc is repetitive and needless.
   Additionally, they can make your front-end code quite messy.
5. The buttons themselves take up a lot of space (especially the Facebook share
   button).

Let's take a quick look at the alternative, using this little plugin:

1. It doesn't load any iframes or extra javascript making the overall load time
   much faster.
2. It looks simple and clean by default, and can be customized in any and every
   way.
3. All you have to do to use it is include the script and call `new ShareButton`
   on a `share-button` element. That's two lines of code total, the script link and the share call.
4. It's tiny and compact, expanding only when the user actually wants to share
   something.

# Getting Started

1. Run `bower install better-share-button#master`. There has not been a release
   of `better-share-button` since its original forking from `share-button`, so
   you need to use the master branch.
2. Make a `share-button` element on your page.
3. In your javascript, call `new ShareButton`.
4. Pass options to the share call if you want (details below).
5. Profit!

```html
<share-button></share-button>
```

```javascript
new ShareButton({
  // Optional options:
  networks: {
    facebook: {
      appId: "abc123"
    }
  }
});
```

## NPM installation

**TODO**

# Customization
## Configuration Options
The share button is extremely flexible. As such, we provide the ability to pass a
wide array of options for additional configuration. All configuration options
are available [here](https://github.com/kirbyfan64/better-share-button/blob/master/docs/configuration-options.md).

## Styles
Additionally, you're able to customize the look and feel of the button and
animations though CSS. All CSS styles and how to modify them are available
[here](https://github.com/kirbyfan64/better-share-button/blob/master/docs/styles.md).

## Hooks
You are able to set `before` and `after` hooks when a user clicks a network.
This allows you to dynamically change attributes for that button. For more
information, see
[here](https://github.com/kirbyfan64/better-share-button/blob/master/docs/network-hooks.md)

# Public API
The share button also returns a simple API that can be used to control it should
you need to. For instance:

```javascript
var share = new ShareButton(); // Grabs all share-button elements on page

share.toggle(); // toggles the share button popup
share.open();   // open the share button popup
share.close();  // closes the share button popup
share.config;   // exposes the configurations listed above
```

# Inspiration
The original `share-button` project was inspired by
[this dribbble shot](http://dribbble.com/shots/1072278) and
[this cssdeck experiment](http://cssdeck.com/labs/css-social-share-button) -
huge props to these two guys for some incredible ideas and work.

This new one was inspired by the original, because it's a fork, and it's kinda
hard *not* to be inspired by the original when you fork!!

# Contributing and License
- Contributing Guidelines can be found
  [here](https://github.com/kirbyfan64/better-share-button/blob/master/CONTRIBUTING.md)
- Licensed under the
  [MIT Expat license](https://github.com/kirbyfan64/better-share-button/blob/master/LICENSE)
