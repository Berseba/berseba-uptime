# berseba-uptime

External uptime monitor for Berseba's CRM (`crm.grupoberseba.com.br`), run by GitHub Actions
every 5 minutes, outside the VPS. When the CRM is down (3 failed checks, 30 s apart) it opens an
issue labelled `fora-do-ar` assigned to the partners — GitHub notifies by e-mail and by the GitHub
mobile app — and closes it with the downtime length when the CRM is back. Weekly it checks the TLS
certificate and commits `heartbeat.txt` so GitHub never disables the schedule.

Public on purpose: Actions minutes are free for public repositories. No secrets are used.
See `.github/workflows/uptime.yml`.
