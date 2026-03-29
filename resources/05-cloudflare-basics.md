# Cloudflare Basics

## What Is Cloudflare?

**Cloudflare** is a company that makes websites faster, safer, and easier to put online. They run one of the biggest networks on the internet — their servers are in cities all over the world, so your website loads quickly no matter where someone is viewing it.

For our purposes, we care about one specific Cloudflare product: **Cloudflare Pages.**

---

## What Is Cloudflare Pages?

**Cloudflare Pages** is a free hosting service for websites. You connect it to your GitHub repo, and every time you push changes, your site automatically updates.

**Why we use it for the portfolio project:**
- It's free (unlimited bandwidth, up to 100 sites)
- It connects directly to your GitHub repo
- It auto-deploys when you push new code
- It gives you a `.pages.dev` URL immediately
- You can add your own custom domain later
- It includes HTTPS/SSL automatically (the lock icon in the browser)

---

## Recommended Resources

### Start Here — Our Exact Workflow

- [Astro + Cloudflare Pages: A Beginner's Guide](https://dev.to/warish/astro-cloudflare-pages-a-beginners-guide-to-fast-and-easy-deployment-558e) — This is the guide that matches our portfolio project setup. It walks through connecting your GitHub repo to Cloudflare Pages and deploying an Astro site step by step.

### Additional Reading

- [So What Is Cloudflare?](https://www.cloudflare.com/learning/what-is-cloudflare/) — Cloudflare's own plain-language explainer
- [Getting Started — Cloudflare Pages Docs](https://developers.cloudflare.com/pages/get-started/) — Official step-by-step setup guide

---

## How It Works (The Big Picture)

```
You write code  →  Push to GitHub  →  Cloudflare detects the push
                                            ↓
                                     Builds your site
                                            ↓
                                     Deploys to their global network
                                            ↓
                                     Your site is live at
                                     your-project.pages.dev
```

Every time you push new code to GitHub, Cloudflare automatically rebuilds and redeploys your site. You don't need to do anything extra.

---

## Key Concepts

| Term | What It Means |
|------|--------------|
| **Static site** | A website made of HTML, CSS, and JavaScript files — no database or backend server needed. Perfect for portfolios. |
| **Deploy** | The process of putting your website online so people can visit it |
| **Build** | The step where Cloudflare turns your project code into the final website files |
| **Custom domain** | Using your own URL (like `tania.design`) instead of the default `.pages.dev` address |
| **CDN** | Content Delivery Network — Cloudflare's network of servers around the world that serve your site from the closest location to each visitor |
| **SSL/HTTPS** | The security certificate that shows the lock icon in the browser. Cloudflare adds this automatically. |

---

## Quick Setup Steps (Preview)

We'll walk through this together in the workshop, but here's the overview:

### Prerequisites

Before connecting to Cloudflare, make sure your Astro project is ready:

1. Your Astro project is in a GitHub repo
2. You can run `npm run build` locally without errors
3. The build output goes to the `dist/` folder (Astro's default)

### Cloudflare Pages Setup

1. Create a free account at [cloudflare.com](https://www.cloudflare.com/)
2. Go to **Workers & Pages** in the dashboard
3. Click **Create** → **Pages** tab
4. Connect your GitHub account
5. Select your portfolio repo
6. Under **Framework preset**, select **Astro** from the dropdown
7. Confirm the build settings for Astro:

| Setting | Value |
|---------|-------|
| **Production branch** | `main` |
| **Build command** | `npm run build` |
| **Build output directory** | `dist` |

8. Click **Save and Deploy**
9. Wait a minute or two — your site is live at `your-project.pages.dev`

### After Deploy

Every time you `git push` to `main`, Cloudflare automatically rebuilds and redeploys your site. No extra steps needed.

---

[← Back to all resources](../README.md)
