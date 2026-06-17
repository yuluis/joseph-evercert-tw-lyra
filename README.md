# joseph-evercert-site

A small welcome page Claude Code built for Joseph. Lives at **[joseph.evercert.io](https://joseph.evercert.io)**.

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
git clone https://github.com/yuluis/joseph-evercert-site.git
cd joseph-evercert-site
claude
```

That last command drops you into a Claude Code session inside the project. Ask it anything — *"change the hero greeting to something I like"*, *"swap the colors to ocean blue"*, *"add a section about my favorite books"*. It will edit the files for you.

## Deploy

The live site is served by nginx on a single vps from `/var/www/joseph.evercert.io/`, which is a git clone of this repo.

To redeploy after pushing here:

```bash
ssh vps "cd /var/www/joseph.evercert.io && sudo git pull && sudo systemctl reload nginx"
```

That's the whole deploy story.

## License

[MIT](./LICENSE). Fork it, ship your own.
