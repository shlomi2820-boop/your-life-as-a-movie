# YOUR LIFE AS A MOVIE — launch starter

This is a mobile-friendly landing page + interactive prototype for the $3 personalized movie poster / short trailer concept.

## What works now
- Responsive landing page
- Name, genre and vibe inputs
- Dynamic poster preview
- Downloadable poster preview PNG generated in the browser
- Share-text action where supported

## What is NOT connected yet
This is a prototype, not a live paid AI service. It does not yet:
- call an AI image-generation API
- create actual AI video/trailer files
- accept real payments
- email or host purchased downloads
- store orders or handle refunds

Do not advertise that customers receive an AI-generated trailer or accept payment until these pieces are integrated and tested.

## Recommended production architecture
1. Frontend: this page, hosted on a static hosting provider.
2. Backend endpoint: creates an order, verifies payment server-side, and only then starts generation.
3. Image generation: server-side API call; keep secret API keys on the server, never in browser JavaScript.
4. Video generation: provider API, queued as a background job. Track status and provide a download link when complete.
5. Payments: choose a provider that explicitly supports a business registered in Israel, international card payments, refunds, and Apple Pay if required. PayPal availability should be tested for the merchant account and target countries.
6. Storage: private object storage with time-limited download links.
7. Safety/privacy: explain how uploaded photos are used and deleted; obtain permission to process and transform the photo; add Terms, Privacy, refund policy, support contact and age policy.

## Suggested launch plan
- Phase 1: use the prototype to test interest with demo posters; do not collect payment.
- Phase 2: add real image generation and make the poster the first paid deliverable.
- Phase 3: add short video generation after measuring per-order cost and reliability.
- Phase 4: connect payments and automated delivery after a full end-to-end test.

## Suggested pricing test
- Poster: $1 (only if payment fees make this viable)
- Poster + 5-second trailer: $3
Keep a strict generation limit per order to avoid runaway API costs. Measure refunds, failed generations, payment fees, and customer support time.

## Before launch
- Confirm business name and domain availability.
- Check tax/business obligations in Israel for global digital sales.
- Configure merchant account, API keys, privacy, terms, refunds and contact email.
- Test checkout, failed payment, duplicate payment, failed generation, refunds and delivery on mobile.
