# OpenClaw Security Checklist

> Please confirm each item before deployment

## Skill Security

- [ ] All installed Skills have been scanned by ClawGuard
- [ ] Skill sources are trusted (official or audited third-party)
- [ ] Regularly check update logs of installed Skills

## Access Control

- [ ] Agent has been configured with the principle of least privilege
- [ ] Sandbox isolation is enabled
- [ ] Unnecessary tool access has been disabled

## Network Security

- [ ] TLS/HTTPS is enabled
- [ ] Gateway port is not directly exposed to the public internet
- [ ] Rate limiting is configured

## Audit Logs

- [ ] All Agent operations are logged
- [ ] Log storage meets compliance retention requirements
- [ ] Sensitive information has been redacted

## Compliance

- [ ] Compliant with Data Security Law requirements
- [ ] Compliant with PIPL (Personal Information Protection Law) requirements
- [ ] CVE-2026-25253 vulnerability has been patched

(To be expanded)
