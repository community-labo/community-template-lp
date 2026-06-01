# Security Policy

This repository is distributed as a static landing page template. It should not contain production secrets, private customer data, or account credentials.

## Supported Use

This template is intended for static HTML/CSS/JavaScript landing pages.

Before publishing a derived site, replace all template values with the actual operator's information:

- Service name
- Pricing and payment URL
- Contact email address
- Specified Commercial Transactions Act information
- Privacy policy operator information
- Google Tag Manager or analytics IDs
- Images and profile details

## Reporting a Vulnerability

If you find a security issue in this template, report it privately to the repository owner or maintainer.

Do not create a public issue containing:

- Exploit details
- Credentials or tokens
- Personal information
- Private business or customer data

When reporting, include:

- A short summary of the issue
- Affected file or feature
- Steps to reproduce, if safe to share
- Suggested fix, if known

## Secrets and Credentials

Never commit secrets to this repository, including:

- Stripe secret keys or webhook secrets
- API keys
- SMTP credentials
- Database credentials
- OAuth client secrets
- Session secrets
- Private `.env` files

Use `.env.example` for placeholder variable names only if environment variables are introduced in the future.

## External Scripts and Tracking

When adding third-party scripts such as analytics, chat widgets, payment widgets, or form tools:

- Use official provider URLs.
- Document the provider and purpose in `README.md`.
- Avoid adding scripts that collect personal data without updating the privacy policy.
- Prefer minimal permissions and minimal data collection.

## Forms and Personal Data

This template currently uses email links instead of a backend form.

If a contact form, checkout integration, CRM integration, or member registration flow is added:

- Do not store personal data in static files.
- Validate and sanitize user input on the server side.
- Add spam and abuse protection where appropriate.
- Update the privacy policy to describe collected data and usage.
- Confirm that data processors and retention rules are appropriate for the operator.

## Deployment Security

For production hosting, configure security headers where supported:

- `Content-Security-Policy`
- `X-Content-Type-Options: nosniff`
- `Referrer-Policy`
- `Permissions-Policy`
- `Strict-Transport-Security` when HTTPS is enforced

Header configuration depends on the hosting provider and is intentionally not hardcoded into these static HTML files.
