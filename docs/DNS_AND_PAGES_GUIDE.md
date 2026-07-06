# EchoSweep GitHub Pages, DNS, and HTTPS guide

Updated: 2026-07-06

## Intended publication model

- Repository: `AdzCodingDev/AdzCodingDev-app_storage_optimizer_org`
- Source branch: `main`
- Source folder: repository root `/`
- Canonical public domain: `echosweep.pl`
- Optional alias: `www.echosweep.pl`
- Repository `CNAME`: `echosweep.pl`

The domain `echosweep.pl` is already verified in the owning GitHub account. Preserve the existing GitHub Pages verification TXT record.

For GitHub Pages on a GitHub Free account, make this website repository public immediately before enabling Pages. Repository visibility, merge, Pages settings, and DNS changes are separate operator actions.

## Recommended publication order

1. Review and merge the website pull request after explicit authorization.
2. Make the website repository public if it is still private and the account uses GitHub Free.
3. In repository **Settings → Pages**, select **Deploy from a branch**.
4. Select branch `main` and folder `/ (root)`, then save.
5. Set the custom domain to `echosweep.pl`.
6. Configure the DNS records below after checking the current DNS zone for conflicts.
7. Wait for DNS checks and certificate provisioning.
8. Enable **Enforce HTTPS** when GitHub makes the option available.
9. Validate all public URLs and redirects before using the privacy-policy URL in Google Play Console.

## DNS records

Use the four GitHub Pages apex A records below, or an equivalent ALIAS/ANAME supported by the DNS provider.

| Type | Host/name | Value | TTL | Purpose |
|---|---|---|---|---|
| A | `@` | `185.199.108.153` | 3600 or provider default | GitHub Pages apex IPv4 |
| A | `@` | `185.199.109.153` | 3600 or provider default | GitHub Pages apex IPv4 |
| A | `@` | `185.199.110.153` | 3600 or provider default | GitHub Pages apex IPv4 |
| A | `@` | `185.199.111.153` | 3600 or provider default | GitHub Pages apex IPv4 |
| CNAME | `www` | `adzcodingdev.github.io` | 3600 or provider default | Optional `www` alias |

Optional IPv6 records currently documented by GitHub:

| Type | Host/name | Value |
|---|---|---|
| AAAA | `@` | `2606:50c0:8000::153` |
| AAAA | `@` | `2606:50c0:8001::153` |
| AAAA | `@` | `2606:50c0:8002::153` |
| AAAA | `@` | `2606:50c0:8003::153` |

Do not use wildcard records such as `*.echosweep.pl` for GitHub Pages.

## DNS safety check

Before editing the zone:

1. inspect all existing records for `echosweep.pl`;
2. replace only records that conflict with the same host and purpose;
3. preserve the existing GitHub domain-verification TXT record;
4. preserve unrelated MX, SPF, DKIM, DMARC, and other TXT records;
5. do not change nameservers unless separately planned and authorized.

## Verification commands

PowerShell:

```powershell
Resolve-DnsName echosweep.pl -Type A
Resolve-DnsName echosweep.pl -Type AAAA
Resolve-DnsName www.echosweep.pl -Type CNAME
```

Expected apex A results:

```text
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

Expected optional `www` target:

```text
adzcodingdev.github.io
```

## HTTPS and live-site validation

After Pages and DNS are configured:

1. confirm GitHub reports the custom-domain DNS check as successful;
2. wait for the TLS certificate to be provisioned;
3. enable **Enforce HTTPS**;
4. verify `http://echosweep.pl/` redirects to `https://echosweep.pl/`;
5. verify the optional `www` address redirects to the canonical apex domain;
6. verify there is no mixed content;
7. open and reread:
   - `https://echosweep.pl/`
   - `https://echosweep.pl/privacy/`
   - `https://echosweep.pl/data-and-permissions/`
   - `https://echosweep.pl/support/`.

DNS propagation and certificate provisioning may take time. Do not classify the site as live until the exact HTTPS pages are accessible and have been reread.
