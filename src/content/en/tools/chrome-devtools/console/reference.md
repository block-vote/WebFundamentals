project_path: /web/tools/_project.yaml
book_path: /web/tools/_book.yaml
description: A comprehensive reference on every feature and behavior related to the Console UI in Chrome DevTools.

{# wf_updated_on: 2019-03-28 #}
{# wf_published_on: 2015-03-28 #}
{# wf_blink_components: Platform>DevTools #}

# Console UI Reference {: .page-title }

{% include "web/_shared/contributors/kaycebasques.html" %}

[API]: /web/tools/chrome-devtools/console/api
[utilities]: /web/tools/chrome-devtools/console/utilities

This page is a comprehensive reference on the Console UI in Chrome DevTools. If you're looking for
the API reference on functions like `console.log()` see [Console API Reference][API]. For the
reference on functions like `monitorEvents()` see [Console Utilities API Reference][utilities].

## Open the Console {: #open }

You can open the Console as a [panel](#panel) or as a [tab in the Drawer](#drawer).

### Open the Console panel {: #panel }

Press <kbd>Control</kbd>+<kbd>Shift</kbd>+<kbd>J</kbd> or
<kbd>Command</kbd>+<kbd>Option</kbd>+<kbd>J</kbd> (Mac).

<figure>
  <img src="/web/tools/chrome-devtools/console/images/panel.png"
       alt="The Console panel."/>
  <figcaption>
    <b>Figure X</b>. The Console panel.
  </figcaption>
</figure>

### Open the Console tab in the Drawer {: #drawer }

[mainmenu]: /web/tools/chrome-devtools/images/shared/main-menu.png

Press <kbd>Escape</kbd> or click **Customize And Control DevTools**
![Customize And Controls DevTools][mainmenu]{: .inline-icon } and then select
**Show Console Drawer**.

<figure>
  <img src="/web/tools/chrome-devtools/console/images/showconsoledrawer.png"
       alt="Show Console Drawer."/>
  <figcaption>
    <b>Figure X</b>. Show Console Drawer.
  </figcaption>
</figure>

The Drawer pops up at the bottom of your DevTools window, with the **Console** tab open.

<figure>
  <img src="/web/tools/chrome-devtools/console/images/drawer.png"
       alt="The Console tab in the Drawer."/>
  <figcaption>
    <b>Figure X</b>. The Console tab in the Drawer.
  </figcaption>
</figure>

## Feedback {: #feedback }

{% include "web/_shared/helpful.html" %}
