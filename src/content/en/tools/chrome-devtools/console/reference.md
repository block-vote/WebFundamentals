project_path: /web/tools/_project.yaml
book_path: /web/tools/_book.yaml
description: A comprehensive reference on every feature and behavior related to the Console UI in Chrome DevTools.

{# wf_updated_on: 2019-03-29 #}
{# wf_published_on: 2015-03-29 #}
{# wf_blink_components: Platform>DevTools #}

[commandmenu]: /web/tools/chrome-devtools/command-menu/#open

# Console UI Reference {: .page-title }

{% include "web/_shared/contributors/kaycebasques.html" %}

[API]: /web/tools/chrome-devtools/console/api
[utilities]: /web/tools/chrome-devtools/console/utilities

This page is a comprehensive reference on the Console UI in Chrome DevTools. If you're looking for
the API reference on functions like `console.log()` see [Console API Reference][API]. For the
reference on functions like `monitorEvents()` see [Console Utilities API Reference][utilities].

This page is organized according to the 2 main uses of the Console: [viewing messages](#view)
and [running JavaScript](#js).

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

To open the Console panel from the [Command Menu][commandmenu], start typing `Console` and then
run the **Show Console** command that has the **Panel** badge next to it.

<figure>
  <img src="/web/tools/chrome-devtools/console/images/showpanelcommand.png"
       alt="The command for showing the Console panel."/>
  <figcaption>
    <b>Figure X</b>. The command for showing the Console panel.
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

To open the Console tab from the [Command Menu][commandmenu], start typing `Console` and then
run the **Show Console** command that has the **Panel** badge next to it.

<figure>
  <img src="/web/tools/chrome-devtools/console/images/showdrawercommand.png"
       alt="The command for showing the Console tab in the Drawer."/>
  <figcaption>
    <b>Figure X</b>. The command for showing the Console tab in the Drawer.
  </figcaption>
</figure>

## View messages {: #view }

TODO this H2 may be unnecessary, but the "Run JS" one seems useful. So maybe convert
these sections into H2s.

### Clear messages {: #clear }

There are many ways to clear the Console:

* Right-click the Console and then select **Clear Console**.
* Type `clear()` in the Console and then press <kbd>Enter</kbd>.
* Call `console.clear()` from your webpage's JavaScript.
* Press <kbd>Control</kbd>+<kbd>L</kbd>.

### Filter messages {: #filter }

#### Filter out messages by URL {: #url }

### Persist logs across page loads {: #persist }

Enable the **Preserve log** checkbox at the top of the console to persist
the console history between page refreshes or changes. Messages will be stored
until you clear the Console or close the tab.

### Save output {: #save }

TODO should this be an H2 section?

Right-click in the Console and select **Save as** to save the output
of the console to a log file.

![Save Console to log file](images/console-save-as.png)

## Disable message stacking {: #stacking }

If a message is consecutively repeated, rather than printing out each
instance of the message on a new line, the Console "stacks" the messages
and shows a number in the left margin instead. The number indicates how many
times the message has repeated.

![Message stacking](images/message-stacking.png)

If you prefer a unique line entry for every log, enable **Show timestamps**
from the DevTools settings.

![Show timestamps](images/show-timestamps.png)

Since the timestamp of each message is different, each message is displayed
on its own line.

![Timestamped console](images/timestamped-console.png)

## Run JavaScript {: #js }



## Select execution context {: #context }

The dropdown menu highlighted in blue in the screenshot below is called the
**Execution Context Selector**.

![Execution Context Selector](images/execution-context-selector.png)

You'll usually see the context set to `top` (the top frame of the page).

Other frames and extensions operate in their own context. To work with these
other contexts you need to select them from the dropdown menu. For example,
if you wanted to see the logging output of an `<iframe>` element and modify
a variable that exists within that context, you'd need to select it from
the Execution Context Selector dropdown menu.

The Console defaults to the `top` context, unless you access DevTools by
inspecting an element within another context. For example, if you inspect
a `<p>` element within an `<iframe>`, then DevTools sets the Execution Context
Selector to the context of that `<iframe>`.

When you're working in a context other than `top`, DevTools highlights the
Execution Context Selector red, as in the screenshot below. This is because
developers rarely need to work in any context other than `top`. It can
be pretty confusing to type in a variable, expecting a value, only to see that
it's `undefined` (because it's defined in a different context).

![Execution Context Selector highlighted red](images/non-top-context.png)

## Settings {: #settings }

TODO cover each setting. Don't have a separate section, like this. Discuss
settings in the context of tasks.

## Feedback {: #feedback }

{% include "web/_shared/helpful.html" %}
