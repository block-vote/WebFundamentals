project_path: /web/tools/_project.yaml
book_path: /web/tools/_book.yaml
description: TODO

{# wf_updated_on: 2019-03-29 #}
{# wf_published_on: 2019-03-29 #}
{# wf_blink_components: Platform>DevTools #}

# Chrome DevTools Command Menu Reference {: .page-title }

{% include "web/_shared/contributors/kaycebasques.html" %}

[VS]: https://code.visualstudio.com/docs/getstarted/userinterface#_command-palette

The Command Menu provides a fast way to navigate the Chrome DevTools UI and accomplish common tasks,
such as [disabling JavaScript](/web/tools/chrome-devtools/javascript/disable).
You may be familiar with a similar feature in Visual Studio Code called the [Command Palette][VS]{: .external }.

<figure>
  <img src="/web/tools/chrome-devtools/javascript/imgs/disable-javascript.png"
       alt="Using the Command Menu to disable JavaScript."/>
  <figcaption>
    <b>Figure X</b>. Using the Command Menu to disable JavaScript.
  </figcaption>
</figure>

## Open the Command Menu {: #open }

[mainmenu]: /web/tools/chrome-devtools/images/shared/main-menu.png

Press <kbd>Control</kbd>+<kbd>Shift</kbd>+<kbd>P</kbd> or
<kbd>Command</kbd>+<kbd>Shift</kbd>+<kbd>P</kbd> (Mac). Or, click **Customize And
Control DevTools** ![Customize And Controls DevTools][mainmenu]{: .inline-icon } and
then select **Run Command**.

<figure>
  <img src="/web/tools/chrome-devtools/command-menu/imgs/runcommand.png"
       alt="Run Command."/>
  <figcaption>
    <b>Figure X</b>. Run Command.
  </figcaption>
</figure>

## See other available shortcuts {: #help }

If you use the workflow outlined in [Open the Command Menu](#open), the Command Menu opens
with a `>` character prepended to the Command Menu text box.

<figure>
  <img src="/web/tools/chrome-devtools/command-menu/imgs/commandcharacter.png"
       alt="The command character."/>
  <figcaption>
    <b>Figure X</b>. The command character.
  </figcaption>
</figure>

Delete the `>` character and type `?` to see other shortcuts that are available from the Command Menu.

<figure>
  <img src="/web/tools/chrome-devtools/command-menu/imgs/shortcuts.png"
       alt="Other available shortcuts."/>
  <figcaption>
    <b>Figure X</b>. Other available shortcuts.
  </figcaption>
</figure>

## Feedback {: #feedback }

{% include "web/_shared/helpful.html" %}
