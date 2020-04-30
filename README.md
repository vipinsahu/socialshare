
# Social Share

**Requirements:** WEB page sharing in different platform like Facebook, Twitter, Instagram and WhatsApp.

Here is my analysis and how we can use share feature of different platform.

## FaceBook Share
A facebook share is when you click the share button to share a piece of content or Web page on Facebook. By adding a special code to a web page you can place a Facebook share button on your web page. When the share button is clicked and the share is posted, the shared content is then published to that user's personal profile (Facebook calls this your "wall").

#### Code Example:
```html
  <div id="fb-root"></div>
  
  <script>
  (function(d, s, id) {
    var js, fjs = d.getElementsByTagName(s)[0];
    if (d.getElementById(id)) return;
    js = d.createElement(s); js.id = id;
    js.src = "https://connect.facebook.net/en_US/sdk.js#xfbml=1&version=v3.0";
    fjs.parentNode.insertBefore(js, fjs);
  }(document, 'script', 'facebook-jssdk'));</script>

  <!-- Your share button code -->
  <div class="fb-share-button" 
    data-href="https://mytesting.com/?mycustom=s1" 
    data-layout="button_count">
  </div>
```
### Facebook uses Open Graph to fetch content from page
```html
  <meta property="og:url"           content="https://mytesting.com/" />
  <meta property="og:type"          content="Just Testing" />
  <meta property="og:title"         content="My Testing Title" />
  <meta property="og:description"   content="My Testing description" />
  <meta property="og:image"         content="https://example.com/img45.png" />
```
### For more information 
Please [click here](https://developers.facebook.com/docs/plugins/share-button/) 

## Twitter Share
It takes as parameters a message text, a Twitter user name, a page URL to share and some tracking parameter values.

#### Code example
```html
<a class="twitter-share-button"
  href="https://twitter.com/intent/tweet?text=Hello%20world%20https://example.com/">
Tweet</a>
```

#### Twitter uses Open Graph and own meta tag to fetch content from page
```html
  <meta name="twitter:card" content="summary" />
  <meta name="twitter:site" content="@nytimesbits" />
  <meta name="twitter:creator" content="@nickbilton" />
  
  <meta property="og:url" content="http://bits.blogs.nytimes.com/2011/12/08/a-twitter-for-my-sister/" />
  <meta property="og:title" content="A Twitter for My Sister" />
  <meta property="og:description" content="In the early days, Twitter grew so quickly that it was almost impossible to add new features because engineers spent their time trying to keep the rocket ship from stalling." />
  <meta property="og:image" content="http://example.com/tmagArticle.jpg" />
```

## WhatsApp Share
It will only work for mobile browser and takes as parameters a message text, a Twitter user name, a page URL to share and some tracking parameter values.
#### Code example
```html
<a href="https://api.whatsapp.com/send?phone=91XXXXXXXXX&text=https://example.com/" target="_blank">WA</a>
```

#### WhatsApp uses Open Graph to fetch content from page
```html
  <meta property="og:url"           content="https://mytesting.com/" />
  <meta property="og:type"          content="Just Testing" />
  <meta property="og:title"         content="My Testing Title" />
  <meta property="og:description"   content="My Testing description" />
  <meta property="og:image"         content="https://example.com/img45.png" />
```

# The Open Graph protocol
The Open Graph protocol enables any web page to become a rich object in a social graph. For instance, this is used on Facebook to allow any web page to have the same functionality as any other object on Facebook.

Please here to get more about the [OG](https://ogp.me/)
