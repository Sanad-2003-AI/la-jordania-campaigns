# La Jordania Campaign Landing Pages

Public static landing pages for La Jordania campaign links.

Current public entry:

- Campaign draft notice: `/`
- Booking form: `/book/`
- GTDIP offer booking link: `/gtdip/`
- GT10 offer booking link: `/gt10/`
- GTCOMBO offer booking link: `/gtcombo/`

Hidden draft campaign links:

- GTDIP offer: `/c/lj-gt-dip-8f42x/`
- GT10 offer: `/c/lj-gt-10-3m91q/`
- GTCOMBO offer: `/c/lj-gt-combo-6p27z/`

Simple test links:

- GTDIP offer: `/gtdip/`
- GT10 offer: `/gt10/`
- GTCOMBO offer: `/gtcombo/`

Preferred production-domain paths once website/DNS access is available:

- `https://lajordania.com.au/offers/lj-gt-dip-8f42x`
- `https://lajordania.com.au/offers/lj-gt-10-3m91q`
- `https://lajordania.com.au/offers/lj-gt-combo-6p27z`

This repo should contain only public campaign landing assets. Do not add POS
exports, strategy docs, private notes, credentials, or customer lists.

The booking form uses approved public contact details and website photos. It
posts attributed booking requests to a hosted form endpoint for server-side
email delivery to the venue, while retaining SMS/email backup actions if the
network request fails.

Lead capture details:

- Endpoint: `https://formsubmit.co/ajax/maikeld1908@yahoo.com`
- Delivery: email to the venue with the offer code, staff instruction, customer
  details, consent flag, source URL, and UTM fields.
- Archive: FormSubmit retains submissions for 30 days and exposes a limited
  archive/export API after the receiving email has confirmed the form.
- First live submission may trigger a FormSubmit email-confirmation step for
  `maikeld1908@yahoo.com`; confirm it before scaling paid traffic.

Each offer link preserves the original clicked offer separately from the final
selected offer in the booking request, so the 14-day test can compare which
offer attracted the enquiry.

Offer-specific links lock the form to that single offer. The generic `/book/`
page can still show all offer options for internal testing.
