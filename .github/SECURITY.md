# Security Policy

## Reporting a Vulnerability

If you find a security issue in Verdesk, **please do not open a public issue**. Email **camilo.brossard@gmail.com** with:

- A short description of the vulnerability.
- Steps to reproduce (a proof-of-concept is welcome but not required).
- The Verdesk version (*Settings → About*) and your Windows version.

You will receive a reply within 72 hours acknowledging receipt. Confirmed issues are patched in the next point release; the reporter is credited in the release notes unless they prefer to stay anonymous.

## Supported Versions

The latest published Release is the only supported version. Older Releases stop receiving security fixes once a newer Release is out.

## Scope

Verdesk runs entirely on the user's machine — there is no Verdesk-controlled server. Reports about:

- Local privilege escalation, sandbox escape, RCE via Verdesk itself, or any path that lets a third party connect or act without the user's approval popup → **in scope**.
- LemonSqueezy License API issues → out of scope here; report to LemonSqueezy directly.
- Issues that require the user to install a separate malicious MCP client themselves → out of scope (Verdesk is the server, not the client).
