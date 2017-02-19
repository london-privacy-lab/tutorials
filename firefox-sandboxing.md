# Setup Sandboxing in Firefox Nightly using Containers

From version 50 of [Firefox Nightly](https://www.mozilla.org/en-US/firefox/channel/desktop/) (not yet rolled out beyond this testing phase) [Mozilla added the ability](https://blog.mozilla.org/tanvi/2016/06/16/contextual-identities-on-the-web/) to compartmentalise identities you use in your browser.

I've found it to be a phenomenal tool and use it every day. It's seperates out session cookies, indexDB, localStorage, and Cache. You can only share this information only across the same container. As long as you keep a tab open, all this data is retained. Once you close all of the container tabs, all the session data is deleted. Immediately opening another tab of the same container, once you've done this, will be an entirely fresh session. Very reassuring level of added control I'm sure you'll agree.

1. Download and open [Firefox Nightly](https://www.mozilla.org/en-US/firefox/channel/desktop/)
2. Open menu (via the hamburger button '≡')
3. Select `Customize`
4. From the left drag `Open Container Tab` to the the customisable menu open on the right
5. Select `Exit Customize`
6. **To open the container menu**
7. Open menu (via the hamburger button '≡')
8. Select `Open Container Tab`
9. **To edit your available containers**
10. From this same menu option select `Manage containers` You can also get here by typing `about:preferences#containers` into the address bar
11. Select `Remove` to delete a container
12. Select `Add New Container` to *shock* add a new one. You could add an emoji (or five) to the name if you wanted to.
13. **To open a new container tab**
14. still writing this 20170219 11:32 UTC
