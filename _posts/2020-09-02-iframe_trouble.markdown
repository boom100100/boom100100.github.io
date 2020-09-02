---
layout: post
title:      "iFrame Trouble"
date:       2020-09-02 14:32:27 -0400
permalink:  iframe_trouble
---


Iframes are great for showing content from another site. Just drop it into your HTML layout and set its source url. Instead of supplying a source url, you can supply the text of a full HTML document within the frame, itself as a source document.

However, iFrames have their limits. They are not the ideal solution for completely replicating dynamic content. Specifically, ads often are restricted from loading due to CORS restrictions. Similarly, content that HTML links to may have CORS restrictions. Also, any relative links in the referenced page will point to the parent document's URL, not the source of the iFrame content. Clicking a link in an iFrame won't load a different page anyway, except if the page opens in a new tab.

CORS restrictions exist in iFrames so that malicious developers are unable to hijack the sessions and data of users. Since this is a security feature, it's necessary for the developer of the referenced website to decide what is an acceptible use of any cross-referencing. Some sites won't allow a browser to load its content in an iFrame at all, whereas some features may be limited.

For developers who want to put an external site in an iFrame, the best they can do is look for what limitations their referenced site developers imposed and work within those.
