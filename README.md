# Recovery & Wellness Massage — Staff Booking Portal

Standalone static site for `booking.recoveryandwellnessmassage.com`. No navigation or dependencies on the public site. Uses the supplied GHL calendar embed.

## Deployment
1. Create a **separate** GitHub repository containing `index.html`, `styles.css`, and `robots.txt` at the root.
2. Import that repository into Vercel as a new project (Framework Preset: Other; no build command).
3. Add `booking.recoveryandwellnessmassage.com` to **this new project's** Domains in Vercel.
4. At your DNS provider, add the `booking` CNAME pointing to the exact target Vercel provides for this project. Do not change the root domain's DNS or the public site's deployment.
5. Verify the calendar loads and create a test booking; confirm appointment and automation behavior in GHL.

## Access and privacy
The page is unlinked, carries a `noindex` robots meta tag, and has a disallow-all robots.txt. These measures DO NOT restrict access. Anyone with the URL can view the embedded booking calendar. For genuine staff-only access, configure Vercel Deployment Protection / an authentication gateway with suitable coverage for the custom production domain, and separately verify GHL booking permissions. The page itself does not implement authentication.

The brand mark is a typographic placeholder because the supplied site ZIP does not include its referenced logo asset. Replace it with an approved logo if desired.

Calendar troubleshooting: The iframe is set to loading="eager" and has no scroll-triggered lazy-loading code. If the calendar remains blank, open the direct calendar link shown below the embed to distinguish GHL calendar availability from iframe/browser issues.
