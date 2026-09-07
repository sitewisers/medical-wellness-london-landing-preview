# Medical Wellness London — Private GP Google Ads Landing Page

**Status: CLIENT PREVIEW ONLY.** Hosted on GitHub Pages for review. Not connected to a live
form endpoint, not on the clinic's domain, and not the version to run ads against.

## Preview fixes applied
- The lead form pointed to a placeholder action (`/YOUR_APPROVED_FORM_ENDPOINT`) that would
  have 404'd on submit. It now redirects to `thank-you.html` on submit so the flow is
  demonstrable, without sending data anywhere. See the comments around the `<form>` and the
  bottom `<script>` in `index.html` — remove the preview redirect and wire in the real
  endpoint before launch.
- The location section used a decorative CSS "map placeholder" div (literally labelled as
  such in the markup). Replaced it with a real embedded Google Map for 61 Mansell Street,
  London E1 8AN, matching the existing container styling.

## What was improved
- Uses a clean Medical Wellness London-style warm cream / neutral / gold visual system.
- Removed the artificial-looking MW logo mark and uses a restrained text wordmark.
- Hero is focused on Private GP + Aldgate + same-day availability subject to availability.
- Uses verified current clinic information from the live site.
- Primary CTA goes to the clinic's current GP booking system.
- Added a short secondary "Request an Appointment" lead form.
- Form intentionally does NOT collect medical information.
- Captures UTM parameters and GCLID so advertising source can be passed into the lead record.
- Added GA4/GTM dataLayer hooks for CTA clicks and lead submission.
- Added a clear urgent-call route.

## IMPORTANT BEFORE LAUNCH
The form currently points to:
`/YOUR_APPROVED_FORM_ENDPOINT`

Replace this with the clinic's approved CRM/form endpoint. Do not use an unapproved third-party form processor for personal/health-related lead data.

Also:
1. Install the client's real Google Tag Manager / GA4 container.
2. Configure Google Ads conversions:
   - completed booking (primary)
   - qualified lead form submission
   - click-to-call / phone call (secondary)
   - WhatsApp click (secondary, if used)
3. Confirm that the booking platform can pass/retain attribution if you want booking-level attribution.
4. Confirm the client's privacy notice covers this landing-page lead capture.
5. Keep the form limited to contact/booking information and instruct visitors not to submit medical information.
6. Verify all final claims before launch.

## Current verified business details
- 61 Mansell Street, London E1 8AN
- 020 4636 7333
- Monday–Saturday, 10am–7pm
- GP consultations from £90
- GMC-registered doctors
- 2 minutes from Aldgate station
- GP booking URL: https://online-booking.semble.io/?token=5181436fdee48fb45b10f6ea0210b040390aa8a6
- Same-day appointments: client-confirmed, subject to availability
