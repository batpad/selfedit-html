# selfedit — an HTML page that edits itself

One HTML file. Open it in your browser, talk to the editor that lives inside
it, and it becomes whatever you want — a homepage, a photo page, a little app.
Then share the file, or host it anywhere. No installs, no build tools, no
server, no account (you bring your own AI model key).

## Get started

1. **Download [`index.html`](index.html)** (rename it to anything you like).
2. **Open it** — double-click it, or drag it into a browser window. Chrome or
   Edge give the smoothest experience (see [Saving](#saving)).
3. Click the **✎ button** in the bottom-right corner, open **⚙ Settings**, and
   paste a model API key. An [OpenRouter](https://openrouter.ai/keys) key is
   the easiest — one key, every model; pick a model with the *Browse* button.
   Any OpenAI-compatible endpoint also works (Ollama or LM Studio running
   locally, etc.).
4. **Ask for things.** *"Make this a homepage for my pottery studio."*
   *"Warmer colors."* *"Add a section about workshops with a signup email."*
   Changes appear instantly; nothing is permanent until you hit **Save**.

The **?** button inside the editor is the full how-to: selecting elements on
the page, editing text by hand, the CSS editor, undo, and more.

## Saving

The page saves **itself, back into the file** — that's the whole trick. How,
depends on where it's open:

- **Chrome / Edge, opened from your disk**: the first Save asks you to pick
  the file (pick the same file you opened); after that it saves in place.
  The browser asks permission once per session.
- **Firefox / Safari**: Save downloads a fresh copy — replace the old file
  with it. Slightly clunkier, works everywhere.
- The ● dot on the ✎ button means you have unsaved changes.

Your API key is **never** saved into the file — it stays in your browser.
The file is always safe to share.

## Sharing what you made

The finished page is just an HTML file:

- **Send the file itself** — email, chat, USB stick. The person you send it to
  can view it like any web page, and even keep editing it with their own key.
- **Host it** — anywhere that serves static files: GitHub Pages,
  Netlify Drop, your own server. Visitors just see your page; the editor
  only wakes up for whoever clicks the ✎.

## A few things worth knowing

- Your page talks **directly** to your model provider. There's no middleman
  server and nothing to sign up for; the only cost is your own API usage.
- The editor itself is loaded by the single `<script>` tag near the top of the
  file. Don't delete it — it's what keeps the page editable. (It guards
  itself, but still.)
- You can also edit the HTML by hand in any text editor, any time. It's your
  file. The built-in editor is even designed to help you learn how: every AI
  edit can be expanded to show the exact HTML it wrote.
- Power users can teach the agent new tools (maps, data sources, your own
  SDK…) with plugins that travel inside the file — see the
  [page-agent](https://github.com/batpad/page-agent) repo, which is where the
  editor itself is developed and where issues belong.
