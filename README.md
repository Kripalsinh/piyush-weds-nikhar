# પીયૂષ સંગ નિખાર — Wedding Invitation Website

A single static page with no build step. The folder contains:

```
index.html        ← the whole website (design, text, animations)
images/
  groom.jpg       ← Piyush
  bride.jpg       ← Nikhar
  couple-1.jpg    ← seaside photo (gallery)
  couple-2.jpg    ← traditional photo (gallery)
  og.jpg          ← preview image shown when the link is shared on WhatsApp
music.mp3         ← (optional) add any song with this exact name and a music button appears
```

## Deploy on Vercel

### Option A: GitHub (easiest to update later)
1. Create a new repository on github.com, for example `piyush-weds-nikhar`.
2. Upload everything in this folder (`index.html` and the `images` folder) using "Add file → Upload files".
3. On vercel.com, click **Add New → Project**, then import that repository.
4. Framework preset: **Other**. Leave the build settings empty and click **Deploy**.
5. Your link will be `https://piyush-weds-nikhar.vercel.app`, or similar.

Any later change you upload to GitHub redeploys the site automatically.

### Option B: Vercel CLI (needs Node.js)
```
npm i -g vercel
cd piyush-weds-nikhar
vercel --prod
```

## After deploying
- **WhatsApp preview:** in `index.html`, the `og:image` line points to
  `https://piyush-weds-nikhar.vercel.app/images/og.jpg`. If your Vercel URL is different, change that line to match your URL.
- **Personalised links per guest:** add `?to=Name` to the end of the link, for example
  `https://piyush-weds-nikhar.vercel.app/?to=રમેશભાઈ`
  The envelope and the letter will then say "સ્નેહી શ્રી રમેશભાઈ". The plain link without `?to=` works for everyone.
- **Maps:** to point each venue at the exact pin, open the place in Google Maps, click Share, copy the link, and replace the `href` of the "દિશા મેળવો" button for that venue in `index.html`.
