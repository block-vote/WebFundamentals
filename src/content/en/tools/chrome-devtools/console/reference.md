project_path: /web/tools/_project.yaml
book_path: /web/tools/_book.yaml
description: A comprehensive reference on every feature and behavior related to the Console UI in Chrome DevTools.

{# wf_updated_on: 2019-04-03 #}
{# wf_published_on: 2015-04-03 #}
{# wf_blink_components: Platform>DevTools #}

[commandmenu]: /web/tools/chrome-devtools/command-menu/

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
run the **Show Console** command that has the **Drawer** badge next to it.

<figure>
  <img src="/web/tools/chrome-devtools/console/images/showdrawercommand.png"
       alt="The command for showing the Console tab in the Drawer."/>
  <figcaption>
    <b>Figure X</b>. The command for showing the Console tab in the Drawer.
  </figcaption>
</figure>

### Open Console Settings {: #settings }

[settings]: /web/tools/chrome-devtools/console/images/settingsbutton.png

Click **Console Settings** ![Console Settings][settings]{: .inline-icon }.

<figure>
  <img src="/web/tools/chrome-devtools/console/images/consolesettings.png"
       alt="Console Settings."/>
  <figcaption>
    <b>Figure X</b>. Console Settings.
  </figcaption>
</figure>

The links below explain each setting:

* [**Hide Network**](#network)
* [**Preserve Log**](#persist)
* [**Selected Context Only**](#filtercontext)
* [**Group Similar**](#group)
* [**Log XmlHttpRequests**](#xhr)
* [**Eager Evaluation**](#eagereval)
* [**Autocomplete From History**](#autocomplete)

## View messages {: #view }

This section contains all features related to controlling how messages are presented in the
Console.

### Disable message grouping {: #group }

[Open Console Settings](#settings) and disable **Group similar** to disable the Console's
default message grouping behavior. See [Log XHR and Fetch requests](#xhr) for an example.

### Log XHR and Fetch requests {: #xhr }

[Open Console Settings](#settings) and enable **Log XMLHttpRequests** to log all
`XMLHttpRequest` and `Fetch` requests to the Console as they happen.

<figure>
  <img src="/web/tools/chrome-devtools/console/images/xhrgrouped.png"
       alt="Logging XMLHttpRequest and Fetch requests."/>
  <figcaption>
    <b>Figure X</b>. Logging <code>XMLHttpRequest</code> and <code>Fetch</code> requests.
  </figcaption>
</figure>

The top message in **Figure X** shows the Console's default grouping behavior. **Figure X** shows
how the same log looks after [disabling message grouping](#group).

<figure>
  <img src="/web/tools/chrome-devtools/console/images/xhrungrouped.png"
       alt="How the logged XMLHttpRequest and Fetch requests look after ungrouping."/>
  <figcaption>
    <b>Figure X</b>. How the logged <code>XMLHttpRequest</code> and <code>Fetch</code> requests
    look after ungrouping.
  </figcaption>
</figure>

### Persist messages across page loads {: #persist }

By default the Console clears whenever you load a new page. To persist messages across page loads,
[Open Console Settings](#settings) and then enable the **Preserve Log** checkbox.

### Filter messages {: #filter }

#### Filter by log level {: #level }

DevTools assigns each `console.*` method a severity level. There are 4 levels: `Verbose`, `Info`,
`Warning`, and `Error`. For example, `console.log()` is in the `Info` group, whereas
`console.error()` is in the `Error` group. The [Console API Reference][API] describes the severity
level of each applicable method. Every message that the browser logs to the Console has a 
severity level too. You can hide any level of messages that you're not interested in.
For example, if you're only interested in `Error` messages, you can hide the other 3 groups.

Click the **Log Levels** dropdown to enable or disable `Verbose`, `Info`, `Warning` or 
`Error` messages.

<figure>
  <img src="/web/tools/chrome-devtools/console/images/loglevels.png"
       alt="The Log Levels dropdown."/>
  <figcaption>
    <b>Figure X</b>. The <b>Log Levels</b> dropdown.
  </figcaption>
</figure>

#### Filter messages by URL {: #url }

Type `url:` followed by a URL to only view messages that came from that URL.
After you type `url:` DevTools shows all relevant URLs. Domains also work. For example, if
`https://example.com/a.js` and `https://example.com/b.js` are logging messages,
`url:https://example.com` enables you to focus on the messages from these 2 scripts.

<figure>
  <img src="/web/tools/chrome-devtools/console/images/urlfilter.png"
       alt="A URL filter."/>
  <figcaption>
    <b>Figure X</b>. A URL filter.
  </figcaption>
</figure>

Type `-url:` to hide messages from that URL. This is called a negative URL filter.

<figure>
  <img src="/web/tools/chrome-devtools/console/images/negativeurlfilter.png"
       alt="A negative URL filter. DevTools is hiding all messages that match the URL
            https://b.wal.co"/>
  <figcaption>
    <b>Figure X</b>. A negative URL filter. DevTools is hiding all messages that match the URL
    <code>https://b.wal.co</code>.
  </figcaption>
</figure>

#### Filter out messages from different contexts {: #filtercontext }

Suppose that you've got an ad on your page. The ad is embedded in an `<iframe>` and is generating
a lot of messages in your Console. Because this ad is in a different [JavaScript
context](#context), one way to hide its messages is to [open Console Settings](#settings)
and enable the **Selected Context Only** checkbox.

### Save output {: #save }

TODO should this be an H2 section?

Right-click in the Console and select **Save as** to save the output
of the console to a log file.

![Save Console to log file](images/console-save-as.png)

### Hide network messages {: #network }

By default the browser logs network messages to the **Console**. For example, the top message
in **Figure X** represents a 404.

<figure>
  <img src="/web/tools/chrome-devtools/console/images/404.png"
       alt="A 404 message in the Console."/>
  <figcaption>
    <b>Figure X</b>. A 404 message in the Console.
  </figcaption>
</figure>

To hide network messages:

1. [Open Console Settings](#settings).
1. Enable the **Hide Network** checkbox.

## Clear the Console {: #clear }

There are many ways to clear the Console:

* Right-click the Console and then select **Clear Console**.
* Type `clear()` in the Console and then press <kbd>Enter</kbd>.
* Call `console.clear()` from your webpage's JavaScript.
* Press <kbd>Control</kbd>+<kbd>L</kbd> while the Console is in focus.

## Run JavaScript {: #js }

### Watch an expression's value in real-time with Live Expressions {: #live }

TODO this should be a separate doc. Link off to it.

If you find yourself typing the same JavaScript expression in the Console repeatedly, you might
find it easier to create a **Live Expression**.

**Live Expressions** enable you to monitor the value of a JavaScript expression in (near)
real-time. 

**Figure X** is an example of using a **Live Expression** to monitor the value of
`document.activeElement` in real-time.

### Disable Eager Evaluation {: #eagereval }

### Disable autocomplete from history {: #autocomplete }

### Select JavaScript context {: #context }

![Execution Context Selector highlighted red](images/non-top-context.png)



## Feedback {: #feedback }

{% include "web/_shared/helpful.html" %}
