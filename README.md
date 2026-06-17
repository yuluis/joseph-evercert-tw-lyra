# joseph-evercert-tw-lyra

A small welcome page Claude Code built for Joseph. Lives at **[evercert.tw/lyra/joseph](https://evercert.tw/lyra/joseph/)**.

It is also a sandbox. Joseph is meant to edit it.

## Structure

Four files, no build step, no framework:

```
content.json   ← the words on the page (edit me)
index.html     ← the structure
style.css      ← the look
hero.svg       ← the little sailboat
```

Open `content.json` to change copy. Open `style.css` to change colors. Open `index.html` to change layout.

## Edit in the browser

1. Open this repo on GitHub.
2. Click the file you want to edit.
3. Click the pencil icon.
4. Make a change. Click *Commit*.

The live site picks it up the next time the deploy runs.

## Edit locally with Claude Code

```bash
git clone https://github.com/yuluis/joseph-evercert-tw-lyra.git
cd joseph-evercert-tw-lyra
claude
```

That last command drops you into a Claude Code session inside the project. Ask it anything — *"change the hero greeting to something I like"*, *"swap the colors to ocean blue"*, *"add a section about my favorite books"*. It will edit the files for you.

## Deploy

The live site is served by nginx on a single vps as a static subdirectory of `evercert.tw`. The path on disk is `/var/www/evercert-tw-landing/lyra/joseph/`, which is a git clone of this repo. Static files win over the React SPA fallback above, so no nginx config change is needed.

To redeploy after pushing here:

```bash
ssh vps "cd /var/www/evercert-tw-landing/lyra/joseph && git pull"
```

No nginx reload required.

## License

[MIT](./LICENSE). Fork it, ship your own.
