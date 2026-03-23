# Dream Director — Landing Page

Live site for [dreamdirector.app](https://dreamdirector.app)

## Files

| File | Purpose |
|------|---------|
| `index.html` | The full landing page — all CSS, JS, and HTML in one file |
| `og-image.jpg` | Social sharing image (used in OG/Twitter meta tags) |

## Deploying via GitHub Pages

1. Push this folder to a GitHub repo
2. Go to repo **Settings → Pages**
3. Set source to **main branch / root folder**
4. GitHub will publish at `https://yourusername.github.io/repo-name`
5. Add your custom domain in Settings → Pages → Custom domain

## Custom domain setup (Namecheap → GitHub Pages)

In Namecheap DNS, add these records:
```
A     @    185.199.108.153
A     @    185.199.109.153
A     @    185.199.110.153
A     @    185.199.111.153
CNAME www  yourusername.github.io
```

Then in GitHub Pages settings, enter `dreamdirector.app` as custom domain.

## Before going live checklist

- [ ] Replace `og-image.jpg` with a proper 1200x630px social sharing image
- [ ] Verify Resend domain is connected and Edge Function is deployed
- [ ] Test waitlist form on live URL
- [ ] Submit to Google Search Console
- [ ] Add Stripe link once KVK registered

## Backend

- **Waitlist storage**: Supabase (project: qcdhkmucgxlhtirxxdxt)
- **Confirmation emails**: Supabase Edge Function → Resend
- **Edge function code**: see `send-confirmation.ts` (not in this repo — lives in Supabase dashboard)
