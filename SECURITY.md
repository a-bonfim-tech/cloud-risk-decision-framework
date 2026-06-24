# Security Policy

## Scope

This repository is a documentation-first cloud risk decision framework. It does
not contain production configurations, live infrastructure, customer data, or
copy-paste deployment guidance.

The repository should remain:

- Publicly shareable
- Vendor-neutral unless explicitly stated
- Free of secrets, credentials, and private identifiers
- Clear about assumptions and uncertainty
- Safe for audit, interview, and governance review

## Reporting a Concern

Open a GitHub issue if you identify:

- Sensitive information
- A risk decision that makes unsupported claims
- A framework mapping that appears inaccurate
- Guidance that could be interpreted as production-ready without validation
- Missing assumptions that materially change the decision

Do not include private organizational data or real incident details in public
issues. Use abstracted examples where possible.

## Triage Process

Reports are handled in this order:

1. Preserve the report and affected file path.
2. Identify whether the concern is factual, methodological, legal, or
   operational.
3. Correct unsupported claims or clarify assumptions.
4. Add references where needed.
5. Record the correction in commit history.

## Intended Use

This framework supports risk reasoning, governance discussion, and security
architecture review. It is not a substitute for legal advice, compliance
attestation, threat modeling for a specific production system, or vendor
documentation.
