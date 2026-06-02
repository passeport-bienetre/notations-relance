# notations-relance

Landing page for the **expired-card reactivation campaign** (Juin 2026 one-shot).

Mirror of [`notations-mai`](https://github.com/passeport-bienetre/notations-mai) with one addition: a "Renouveler ma carte" CTA on the thank-you screen pointing to <https://www.bodypass.ch/commande/>.

## Audience

- Mailchimp segment: `Reactivation - Expires + Visites 12M (sans Notations Mai)` (~514 contacts)
- Filter: `STATUT_CRT = expired AND VISITES12M > 0 AND a pas reçu Notations Mai 2026`

## URL

`https://passeport-bienetre.github.io/notations-relance/?t=*|USER_TOKEN|*`

## Notes

- One-shot: this repo is NOT in the daily Moteur Campagne cron.
- JSONs in `data/` are a snapshot copied from local `review-data/` (generated 2 juin 2026).
- USER_TOKEN values for the expired audience were uploaded once to Mailchimp via CSV import (the engine's `build_user_tokens_csv` only covers actives by default, so this had to be done manually).
