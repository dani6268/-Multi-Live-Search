# Homepage

### Custom Start/home page (multi LIVE Search) with live animated weather and news ticker -  written in HTML/JS. Minimal, self-hosted, and dope.
<br>

**DEMO**:  https://seanvree.github.io/homepage/

**Last Updated**: 17 NOV 2019:
- Added Google Analytics (**Action Required**).
- Code maintenance.
- Updated jQuery, Bootstrap.


# Features:

- Self hosted, VERY minimal(ish)/lightweight.
- Live searching.
- Customizable Bookmarks.
- Mobile ready.
- Fully functional multi-search input form (Google, YouTube, Wiki, IMDB).
- Live custom news ticker provided by: feed.mikle.com ($1/month).
- Background auto change (day/night).
- Monthly calendar modal (Click on date) (Appears only on desktop browsers - screen height > 730px).
- Live DTG with click-to-convert time (12/24hr).
- Weather data auto generated via Geolocation.
- Weather API provided via OpenWeatherMap.
- Click-to-convert Celsius/Fahrenheit.
- 5-day forecast data (Click on right weather icon).
- Page hit counter (PHP) (bottom right).
- Stand-alone weather app can be found here:  https://github.com/seanvree/Weather
- Check out my other self-hosted apps here:  https://github.com/Monitorr

<br>

## Screenshot Desktop:

<img src="https://i.imgur.com/WkiO88x.gif">

## Screenshot Mobile:

<img src="https://i.imgur.com/MAlKhhB.gif">

## Animated Weather Icons :

<img src="https://i.imgur.com/0iamcsT.gif[/img]">

# Notes:

- Add desired background image files:

**`/css/main.css`: LINE 38 & 55**:

```
background: url("background_day.jpg");
```

_NOTE_: Background DAY displays from 0800-2000 local browser time


- Turn ON search auto-complete by changing the value to `< "autocomplete="ON" >` at the following location:

**`/index.html`: LINE 265:**

```
<input type="search" id="flexbox-input" name="s" value="" placeholder=" Search..." autocomplete="off" spellcheck="false" autofocus>
```

### WEATHER DATA: 
- Acquire your FREE API key at https://home.openweathermap.org/users/sign_up
- Replace the default key:

**`/js/weather.js` : LINE 12:**
 
```
   var weatherApiKey = ' YOUR KEY HERE ';
```

- Change the default temp unit from F to C by changing the following two items:

**`/index.html`: LINE 128:**

```
<div id="unit" class="unit hidden">&degF</div>
```

**`/js/weather.js`: LINE 8:**

```
var unit = 'metric';
```

- Weather auto refresh default setting is  **30** seconds (2 calls per minute), or 30000(ms). Max is 60 API calls per 1 minute. Change at the following location:

**`/js/weather.js` : LINE 201:**

```
var t = window.setInterval(searchByLocation, 30000);
```

### TICKER DATA: 
- Create a customized feed.mikle ticker widget for RSS news sources and style.  Go to https://feed.mikle.com, create an account, and replicate the settings of the screenshot image `/img/feedmikle.jpg ` located in this repo.  
- Input the custom ticker widget URL at the following location:

**`/index.html` : Line 293**:
 
 ```
 <script src="https://feed.mikle.com/js/fw-loader.js" data-fw-param=" YOUR NUMBER HERE "></script>
 ```

### GOOGLE ANALYTICS:
- Acquire a FREE Google Analytics site ID at: https://analytics.google.com/ 
- Replace the default site ID `UA-XXXXX-Y` at the following location:

**`/js/analytics.js` : LINE 9**:
 
```
   ga('create', 'UA-133756821-1', 'auto');
```

## LIVE Search Usage:

### Key Searching:

- Make changes to the live search behavior and/or bookmarks in `/js/tilde.js` .
- When using commands, the desired result MUST be selected from the suggestions result list below the input field.
- To view the bookmarks and site keys, press `?` for the help menu.

(NOTE: The help menu only appears on desktop browsers).

Search any of the sites by typing a colon after the site's key, followed by a search query.

For example:

- Entering `g:tilde` would search
  [GitHub for tilde](https://github.com/search?q=tilde).
- Entering `s:radiohead` would search
  [SoundCloud for radiohead](https://soundcloud.com/search?q=radiohead).

If an input doesn't match any of the commands, a generic Google search will be triggered.

### Specific Locations:

Navigate directly to a specific location by typing a forward slash after the site's key, followed by the location on the site.

For example:

- Entering `r/r/startpages` would redirect to
  [www.reddit.com/r/startpages](https://www.reddit.com/r/startpages)
- Entering `h/popular` would redirect to
  [hypem.com/popular](http://hypem.com/popular)

### URL Redirects:

If a full domain is entered into the search field, the browser will be redirected to that domain or URL.

For example:

- Entering `stallman.org` would redirect to:
  [stallman.org](https://stallman.org/)
- Entering `https://smile.amazon.com` would redirect to:
  [smile.amazon.com](https://smile.amazon.com/)


<br>

## About Me:

- [seanvree](https://github.com/seanvree) (Windows Wizard)

- I usually hang out here [![Discord](https://img.shields.io/discord/102860784329052160.svg)](https://discord.gg/j2XGCtH)

- Buy me a beer [![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://paypal.me/monitorrapp)


## Credits:

 [haltdev](https://github.com/haltdev) | [jonfinley](https://github.com/jonfinley) | [leram84](https://github.com/leram84) | [causefx](https://github.com/causefx) | [cadejscroggins](https://github.com/cadejscroggins) 

#

#### Featured on: https://startpages.github.io/

[![BrowserStack Status](https://i.imgur.com/Pnri9gE.gif)](https://automate.browserstack.com/)


<p>
    <a href="https://jigsaw.w3.org/css-validator/check/referer">
        <img style="border:0;width:88px;height:31px"
            src="https://jigsaw.w3.org/css-validator/images/vcss-blue"
            alt="Valid CSS!" />
    </a>
</p>



