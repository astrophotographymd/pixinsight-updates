# Install and use AstroMD Social Export

- Suggested path: `/pages/social-export-guide`
- SEO title (29 chars): Install AstroMD Social Export
- Meta description (152 chars): Add the AstroMD update repository in PixInsight, install Social Export, enter your license key, and export social media files. Includes troubleshooting.

## Add the update repository

This is the usual way to install the script and to get new versions.

1. Open PixInsight.
2. Go to Resources > Updates > Manage Repositories (the exact wording can vary slightly by version).
3. Click Add and enter this URL, including the trailing slash:

   `https://updates.astrophotographymd.com/`

4. Click OK.
5. Go to Resources > Updates > Check for Updates.
6. When an update is offered, install it and restart PixInsight if you are asked to.

The URL must be exactly that address, with https, and with no extra path. PixInsight reads `updates.xri` at that URL and will not follow a redirect.

After a successful install, the script appears under Script > Astrophotography MD > Social Export.

If the menu entry does not appear, open Script > Feature Scripts... and click Regenerate.

## Enter a license key

The free version is ready as soon as the script is installed. You only need a key if you bought the full version.

1. Run Script > Astrophotography MD > Social Export on an open, stretched image.
2. Click Enter license key (the button label may also read License... after you are licensed).
3. Type the email address from your order, and the key from your receipt. The key looks like `ASMD-XXXX-XXXX-XXXX-XXXX`.
4. Click Unlock. The banner at the top of the right column should read "Licensed to" followed by your email.

Use the same email that appears on the order. Capitalization and spaces are ignored. You do not need to be online for the check.

The key may be used on up to two computers, on the honor system. Remove license returns that computer to the free version. Your saved settings stay.

If Unlock is rejected, check for a typo in the email or the key, and try again. If it still fails, email astrophotographymd@gmail.com with the order number (do not post your key in a public forum).

## Manual install (optional)

If you cannot use the repository, you can install from a zip:

1. Copy the `AstroMD-SocialExport` folder somewhere stable, for example `Documents/PixInsight Scripts/AstroMD-SocialExport`.
2. In PixInsight, open Script > Feature Scripts...
3. Click Add, choose that folder, then click Done.
4. The script should appear under Script > Astrophotography MD > Social Export.

To update by hand later, replace the `.js` file in the same folder and click Regenerate in Feature Scripts if the menu looks out of date. The repository path above is the easier way to stay current.

## Use Single exports

1. Open your finished image and click it so it is the active window. It should be stretched (nonlinear). The preview shows real pixel values, so a linear image will look black, and the script will warn you if it looks linear.
2. Run Script > Astrophotography MD > Social Export.
3. In Targets, check the platforms you want. Click a target to edit its crop box. In the free version, only Instagram targets can be checked.
4. In Images (Single exports only), the current image is checked. With a license, you can check other open images. Click a row to switch the preview and set that image's crop and base name. Each image keeps its own crop per target.
5. Place the crop box: drag inside to move it, drag a corner to resize, use the mouse wheel to grow or shrink it (Shift for fine steps), or click outside the box to center it on that point. Center, Max size, Reset, and Same center for all are under the preview.
6. In Output, confirm the folder (it defaults to a `Social` subfolder next to your image), the base name, and the file name template. Existing files are not overwritten unless you check Overwrite existing files.
7. Optional: open Processing for resampling and sharpening, and Watermark / signature for your own text or logo (licensed).
8. Click Export. The Process Console shows each step. With several images, the status reads like "Image 2 of 3, preset 4 of 7."

## Use Carousel

Carousel export is part of the full version. You can still preview and arrange slides without a license.

1. Switch to Carousel.
2. Pick a Platform (Instagram, TikTok, Facebook, Threads, X, or Custom). The short note under the list has a fixed height; the full note is in the tooltip.
3. Choose a slide shape and a layout: panorama, 2x2 grid, or 3x3 grid, plus detail slides if you want them.
4. Arrange the slide list, then click Export (licensed). Every slide in a set shares one shape so they match in the app.

## Troubleshooting

**The script is not in the Script menu.**
Run Check for Updates again, then Script > Feature Scripts... and click Regenerate. Confirm the repository URL is `https://updates.astrophotographymd.com/` with no typo.

**Check for Updates does not find the repository.**
Confirm the URL uses https and a trailing slash, and that it does not redirect. In a browser, `https://updates.astrophotographymd.com/updates.xri` should load as a short XML file. If DNS for the `updates` host is not set up yet, wait until that record is in place.

**The dialog is too tall, or a slider appears on the right.**
Version 1.3.1 sizes the window to the settings column, up to about 95% of the screen, and hides the right-column scrollbar when the content fits. Update to 1.3.1 or later if you are on an older copy.

**The license key is rejected.**
Use the exact order email and key. Try again without extra characters. If it still fails, email astrophotographymd@gmail.com with the order number.

**The preview looks black.**
The image is probably still linear. Stretch it first, then run the script on the stretched view.

**A target or image is marked "Unlock with a license."**
That item is part of the full version. Enter a key to check it, or uncheck it and use the free Instagram export.

**I need a copy on a second computer.**
You may use the same key on up to two computers, on the honor system. Install from the same repository, then enter the same email and key.

## Support

Email astrophotographymd@gmail.com. Please include your PixInsight version, operating system, and the script version shown in the dialog title (currently 1.3.1).

Related pages: [product page](/pages/social-export), [EULA](/pages/social-export-eula), [digital refund policy](/pages/digital-refund-policy).
