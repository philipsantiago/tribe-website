# Tribe marketing site

Static, dependency-free landing page (`index.html`, `styles.css`, `script.js`).
Layout follows the Wispr Flow pattern (pill nav, big serif hero, tilted ribbon,
interactive proof, dark privacy band, FAQ accordion, closing CTA). Type is
Instrument Serif and Satoshi; colours come from `design/illustrations/palette.css`
and the mascot style sheet. Mascot PNGs are copied from `design/monkey-mascots/png/2x/`.

Run locally:

```sh
python3 -m http.server 4321 --directory website
```

The waitlist form calls `public.join_waitlist(p_email)` on the hosted Supabase
project with the publishable key (migration `20261006204153_waitlist.sql`). The
table has RLS on and no client access; read sign-ups in the dashboard. Until that
migration is on the hosted project the form shows "Something went wrong".
