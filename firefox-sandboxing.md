I'm doing this right now 20170219 10:38 UTC

# Setup Sandboxing in Firefox Nightly using Containers

From version 50 of [Firefox Nightly](https://www.mozilla.org/en-US/firefox/channel/desktop/) (not yet rolled out beyond this testing phase) [Mozilla added the ability](https://blog.mozilla.org/tanvi/2016/06/16/contextual-identities-on-the-web/) to compartmentalise identities you use in your browser.

I've found it to be a phenomenal tool and use it every day. It's seperates out session cookies, indexDB, localStorage, and Cache. You can only share this information only across the same container. As long as you keep a tab open, all this data is retained. Once you close all of the container tabs, all the session data is deleted. Immediately opening another tab of the same container, once you've done this, will be an entirely fresh session. Very reassuring level of added control I'm sure you'll agree.

1. Download [Firefox Nightly](https://www.mozilla.org/en-US/firefox/channel/desktop/)
