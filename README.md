# Matic sales performance

One password-protected page: **Robots/** — robots sold and shipped by month, quarter
and year, with cancellations, returns and the open order book.

Deliberately a SEPARATE site from the production backlog
(shaf-presswala.github.io/backlog). Different audience, different password: the
production team watches shipping queues, this is the sales curve.

## Why the file looks like noise

It is **AES-256-GCM ciphertext**, key derived from the password by PBKDF2-SHA256 at
310,000 iterations, decrypted in the browser. No plaintext is committed here.

## Regenerating

Published by `publish-backlog-git.sh` in `~/Matic Scripts/Shopify`, which regenerates
this page hourly — its figures run through yesterday, so they cannot change more often
than daily.

Password lives in `~/Matic Scripts/.env` as `ROBOTS_PAGE_PASSWORD`.
