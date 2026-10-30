# The A-List, mapped

Live at https://a-list.dasbot.com

A single static page: `index.html` plus a local `avatars/` folder.

## Upload

Copy the whole folder to any static host, keeping these paths together:

```
index.html
avatars/            (1903 portrait thumbnails)
CREDITS.md
a-list.txt          (the source list, not loaded by the page)
```

There is no build step and no server-side code. Open `index.html` from the folder root. All image paths are relative, so the page also works in a subdirectory or straight from `file://`.

## How the portraits work

The page opens on a random well-connected person, zoomed in. The fit button shows the whole map. The **Scientologists** toggle highlights the 26 people whose entries describe them as Scientologists. Portraits are lazy-loaded as you zoom in; the overview is static and starts with the original coloured dots, then keeps any portraits already loaded. Cards open on click or from search — not on hover — and load the portrait on demand. Each card has a Wikipedia link, or a Wikipedia search link when no article exists. The files are 160×160 WebP thumbnails.

1894 of the 1903 people have a portrait from Wikipedia/Wikimedia or IMDb. The other 9 use a generated placeholder avatar because no reliable portrait was found. `CREDITS.md` lists the source for every file; `avatars/manifest.json` contains the same data in machine-readable form.

The portraits remain the property of their original photographers, studios, publishers and estates. They are used here only to identify the people named in the gossip list, which is itself unverified hearsay.

## Sharing a person

Each card has a **Share** button. Links look like `https://a-list.dasbot.com/#tom-cruise` and open the map on that person with their card showing. On phones the button opens the share sheet; elsewhere it copies the link. The address bar follows whichever card is open, so copying it works too.

## One flagged hoax

**Susanna Eng** is a known internet hoax: no such actress, model or producer existed, and the claims attached to the name were fabricated. Her node is kept on the map only to show what the list claimed, and her card is marked **Hoax**.
