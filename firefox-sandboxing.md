# Setup Sandboxing in Firefox Nightly using Containers

From version 50 of [Firefox Nightly](https://www.mozilla.org/en-US/firefox/channel/desktop/) (not yet rolled out beyond this testing phase) [Mozilla](https://www.mozilla.org/) [added the ability](https://blog.mozilla.org/tanvi/2016/06/16/contextual-identities-on-the-web/) to compartmentalise identities you use in your browser.

I've found it to be a phenomenal tool and use it every day. It's seperates out session cookies, indexDB, localStorage, and Cache. You can only share this information only across the same container. As long as you keep a tab open, all this data is retained. Once you close all of the container tabs, all the session data is deleted. Immediately opening another tab of the same container, once you've done this, will be an entirely fresh session. Very reassuring level of added control I'm sure you'll agree.

1. Download and open [Firefox Nightly](https://www.mozilla.org/en-US/firefox/channel/desktop/)
2. Open menu (via the hamburger button '≡')
3. Select `Customize`
4. From the left drag `Open Container Tab` to the the customisable menu open on the right [You could alternatively drag this to your toolbar. It will save you a click every time by adding it to the toolbar]
5. Select `Exit Customize`
6. **To open the container menu**
7. Open menu (via the hamburger button '≡')
8. Select `Open Container Tab` [Or if you dragged containers to your toolbar, simply click its icon, then select the container session you wish to open in a new tab]
9. **To edit your available containers**
10. From this same menu option select `Manage containers` You can also get here by typing `about:preferences#containers` into the address bar
11. Select `Remove` to delete a container
12. Select `Add New Container` to *shock* add a new one. You could add an emoji (or five) to the name if you wanted to.
13. **To open a new container tab**
14. Open menu (via the hamburger button '≡') [Or click on the container icon you dragged to your toolbar]
15. Select the container option you wish to use
16. Note that this will open a new tab and not perform this action in the current tab
17. As a benefit to your privacy, you can not open a currently open tab in a different container. This bugged me for a little while, but this is a beneficial feature of containers.
18. **To open a webpage URL in a specific container**
19. Right-click the url
20. Select `Open Link in New Container Tab`
21. Select your desired container option
22. **or if you have a ton of tabs open**
23. Select the new `List all tabs` arrow down icon that appears to the right in the tab menu
24. Select `New container tab`
25. Select your desired container session or `manage containers` to edit or delete
26. **To move the location of the Containers icon**
27. Currently you can only have in either the hamburger menu, or the toolbar, not both at once
28. To swap location, open menu (via the hamburger button '≡')
29. Drag the 'Open container tab' icon to your desired location
30. Select `Exit customize`
 
As [Firefox Nightly](https://www.mozilla.org/en-US/firefox/channel/desktop/) is even before [Firefox Beta](https://www.mozilla.org/en-US/firefox/beta/all/) you might find things occasionally break. With that in mind, however, it is the most actively updated version of Firefox around. Many [Mozillians](https://wiki.mozilla.org/Mozillians) use Nightly as their everyday browser. 

Do keep in mind that you might struggle to open a variety of versions of Firefox simultaneously. ~~This can be acheived a simple terminal command `--no-remote`. So for example `firefox --no-remote`~~ [Edit: this does not work for me, does anyone know how to acheive this?]

