# Statuslog Micro.blog plugin
Display your omg.lol Statuslog on a micro.blog page.

![](https://github.com/gr36/status-log/raw/main/docs/nowpage.png)

## Changelog
- 1.0 Initial release
- 1.0.1 Inprove styling and scripting
- 1.1 Remove all on page scriting and instaed use Hugo Getdata

## Set Up
Instal the plugin from Github by clicking design, edit theme, and then add new plugin.

Call the plugin anything you wish, copy in the URL from the Github page, and click Add Plugin.

### Add Shortcode
Add the partial to the page you wish this to show on, for example, I have placed this on my home page but you could do this wherever you like.

Simply add ```{{< statuslog >}}``` to your page wherever you want the updates to appear.

### Configuration

You *must* change the account name in the plugin configuration to your own, otherwise Adams statues will appear on your page! Whilst you are there you can choose how many statuses you want to appear on the page.

![](https://github.com/gr36/status-log/raw/main/docs/config.png)

## Styling
There is absolutely no styling applied to the div elements placed on the page. This is to give you the most choice possible for how it looks. In my example screenshot above I have some very simple flexbox styling as shown below.

```
#omg_statuslog {
    display: flex;
    flex-direction: column;
    gap: 20px;
    font-size: 80%;
}

#omg_statuslog > div:nth-child(1) {
    background: blue;
    border-radius: 11px;
    color: white; 
}

#omg_statuslog > div {
        display: flex;
        justify-content: space-between;
        padding: 10px;
        flex-direction: row;
        flex-wrap: nowrap;
        gap: 20px
}

#omg_statuslog .status_emoji {
    font-size: 50px;
}

#omg_statuslog .status_content {
    flex: 80%;
}
```

## Considerations
~~This plugin uses on page javascript so there are a few things to bear in mind.~~ 
- ~~it takes a few seconds to fetch the data from the API and display this on the page~~ No longer the case
- ~~if a browser is setup to blog javascript then nothing will appear on the page.~~ No longer the case

## Credits
Thanks to Adam for creating such a great service in omg.lol. The statuslog is just a small part of the service, check it out [here](https://home.omg.lol).

## Support Me
If you found this plugin useful, please consider [buying me a coffee](https://www.buymeacoffee.com/gregmorris)

Check out my other plugins for micro.blog
- [Search Partial](https://github.com/gr36/search-partial)
- [Reply Count](https://github.com/gr36/reply-count/)
