# AstroMD Social Export

- Suggested Shopify / website path: `/pages/social-export`
- SEO title (36 chars): AstroMD Social Export for PixInsight
- Meta description (143 chars): Turn a finished PixInsight image into social media files in one step. Free Instagram exports, or unlock every platform and carousels for $9.99.
- Buy price: $9.99, one-time license
- Draft Shopify product should stay in Draft until Jim publishes it

## JSON-LD (SoftwareApplication)

Place this in the page head or as a JSON-LD script tag. Do not add aggregateRating or review markup.

```json
{
  "@context": "https://schema.org",
  "@type": "SoftwareApplication",
  "name": "AstroMD Social Export",
  "description": "Turn a finished PixInsight image into social media files in one step. Free Instagram exports, or unlock every platform and carousels for $9.99.",
  "applicationCategory": "MultimediaApplication",
  "operatingSystem": "Windows, macOS, Linux",
  "softwareVersion": "1.3.1",
  "author": {
    "@type": "Organization",
    "name": "Astrophotography MD LLC",
    "url": "https://www.astrophotographymd.com"
  },
  "offers": {
    "@type": "Offer",
    "url": "https://www.astrophotographymd.com/products/astromd-social-export",
    "price": "9.99",
    "priceCurrency": "USD"
  }
}
```

The product handle may change if Shopify assigns a different one. Update the offer URL to match the live product URL before publish. Do not put this schema on a public page while the product is still a draft.

## Screenshots needed

These are not on the page yet. Shoot them in PixInsight on Windows, then hand them to the coding agent. Do not use placeholder photos or invented UI shots.

1. Single exports: the dialog on a finished image, with the crop box on the preview and the Targets list visible.
2. The Images list with more than one open image, one row selected, showing that each image keeps its own crop.
3. Carousel mode: a panorama or a 2x2 grid with tile numbers visible.
4. The free-version banner and a locked target or image marked "Unlock with a license."
5. A short Process Console or summary after a successful export, plus a file explorer view of the named JPEG files.

Suggested alt text style: "AstroMD Social Export in PixInsight, Instagram Portrait crop on a finished image."

## Hero

# Turn a finished image into social files in one step

AstroMD Social Export is a PixInsight script that crops, resizes, and saves social media files from a stretched image. You pick the platforms, place a crop box for each one, and click Export.

The free version gives you unlimited Instagram exports, with a small AstroMD Social Export credit on each file. A $9.99 license key, paid once, unlocks every platform, custom presets, your own watermark, batch export of several open images, and carousel export.

[Buy the license, $9.99](#buy)

Works inside PixInsight 1.8.9 and later, including 1.9.x.

## Free vs full

| Feature | Free | Full ($9.99 license) |
| --- | --- | --- |
| Single exports | Unlimited | Unlimited |
| Platforms | Instagram presets only. Other targets are visible but locked, with an "Unlock with a license" note. | All built-in platforms, plus custom presets |
| Several open images in Single exports | The current image only. Other open images are listed and marked "Unlock with a license." | Check any open images. Each keeps its own crop and base name. One Export writes every checked image for every checked target |
| Watermark | A small "AstroMD Social Export" credit is added at the bottom right. It cannot be removed or changed. | Your own text or logo, any position |
| Carousel, panorama, grid, and detail slides | You can preview and arrange them | Preview and export |
| Sharpening and file size control | Yes | Yes |

## What it does

- Built-in sizes for Instagram, Facebook, TikTok, Threads, X, and Pinterest, plus custom presets in the full version.
- A crop box for each target, with the aspect ratio locked. Each target, and each open image, remembers its own crop while the dialog is open.
- Resize to the platform's exact pixels, optional sharpening, conversion to sRGB, and a JPEG quality search that stays under the file size target you set.
- Carousel mode for a numbered set of matching slides, including a seamless panorama or a 2x2 or 3x3 grid.
- Updates through the PixInsight update repository, so new versions install from Resources > Updates.

## Buy the license

A license key is $9.99, paid once. It is not a subscription.

After you check out, you will receive a key by email at the address on the order. Enter that email and key in the script under Enter license key. The same key may be used on up to two computers, on the honor system. See the [EULA](/pages/social-export-eula) and the [install guide](/pages/social-export-guide) for details.

[Buy AstroMD Social Export, $9.99]

If you would rather try it first, add the update repository and use the free Instagram export. You can enter a license later without reinstalling.

## Requirements

- PixInsight 1.8.9 or later, including 1.9.x
- Windows, macOS, or Linux (it runs inside PixInsight)
- We have tested the current version on Windows. We have not yet tested it on a Mac or Linux machine of our own.

## How to get started

1. In PixInsight, open Resources > Updates > Manage Repositories and add `https://updates.astrophotographymd.com/`
2. Run Resources > Updates > Check for Updates, install, and restart PixInsight if you are asked to.
3. Open Script > Astrophotography MD > Social Export.
4. If you bought a license, click Enter license key and paste the email and key from your receipt.

The [install and user guide](/pages/social-export-guide) has the full walkthrough, troubleshooting, and a manual zip install if you need it.

## FAQ

**Is there a free version?**
Yes. You can export unlimited Instagram files with a small AstroMD Social Export credit on each one. You do not need a key for that.

**What does the $9.99 license unlock?**
Every built-in platform, custom presets, your own watermark, exporting several open images at once, and carousel export (including panorama, 2x2, and 3x3 grids).

**Is it a subscription?**
No. It is a one-time purchase.

**Which email do I use for the key?**
Use the email address on the order. Capitalization and extra spaces are ignored.

**Can I use the key on more than one computer?**
Yes, on up to two computers, on the honor system. That is meant for a desktop and a laptop, or a tower and a mini PC, that you use yourself. If you need a different arrangement, email astrophotographymd@gmail.com.

**Does it work on a Mac or on Linux?**
It should, because it is a standard PixInsight script. We have tested it on Windows. Mac and Linux have not been tested on our hardware yet.

**How do I get updates?**
Add `https://updates.astrophotographymd.com/` once under Resources > Updates > Manage Repositories. After that, Check for Updates will offer new versions.

**What if it will not install or run?**
See the [install guide](/pages/social-export-guide) and our [digital refund policy](/pages/digital-refund-policy). Support is astrophotographymd@gmail.com.

**Is this an official PixInsight product?**
No. AstroMD Social Export is made by Astrophotography MD LLC. It is not affiliated with, certified by, or endorsed by Pleiades Astrophoto.

## Support

Questions: astrophotographymd@gmail.com

Astrophotography MD LLC, Ohio, United States.
