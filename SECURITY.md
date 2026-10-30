# Security Policy

Aragon X AG maintains the Aragon OSx and aragonOS smart contract frameworks and their official plugins. These contracts govern and protect real assets held by DAOs, so we treat security reports as a top priority and value the work of researchers who help keep them safe.

This policy applies to every repository under [github.com/aragon](https://github.com/aragon) unless a repository publishes its own `SECURITY.md`.

## Reporting a vulnerability

**Please do not open a public issue, pull request or discussion, and do not share details with third parties.**

Report privately through one of these channels:

1. **GitHub private vulnerability reporting (preferred):** on the affected repository, open the *Security* tab and click *Report a vulnerability*.
2. **Email:** [sirt@aragon.org](mailto:sirt@aragon.org).

### Active exploits and emergencies

If you believe a vulnerability is being actively exploited, or funds are at immediate risk:

- Email [sirt@aragon.org](mailto:sirt@aragon.org) with **`[URGENT]`** at the start of the subject line, and

Urgent reports are acknowledged within 24 hours.

### What to include

- Affected repository, contract(s) and version or commit hash
- Network and contract address, if deployed contracts are affected
- A description of the vulnerability and its root cause
- A proof of concept, ideally a Foundry or Hardhat test running against a local fork
- The impact: what an attacker can achieve, under which preconditions, and an estimate of funds at risk
- A suggested fix (optional)

### AI-assisted reports

We welcome findings discovered with the help of AI tools. Every report must still be reviewed and validated by a human before submission and include a working proof of concept or a precise, verifiable explanation. Speculative, unverified or bulk-generated reports will be closed without a detailed response, and repeated low-quality submissions may lead to exclusion from the bug bounty program.

## Scope

Examples of issues we are especially interested in:

- Unauthorized execution of DAO actions or transfer of DAO funds
- Bypassing or escalating the permission system, such as obtaining a permission that was never granted or using one outside its conditions
- Manipulating proposal creation, voting, tallying or execution, such as double voting, vote weight manipulation or executing a proposal that did not pass
- Plugin installation, update or uninstallation flows that grant unintended permissions
- Proxy or upgrade issues that allow taking over, or permanently bricking, a DAO or plugin
- Permanent freezing of funds or permanent denial of service of governance

### Out of scope

- Third-party plugins, integrations and forks not maintained by Aragon
- Attacks that require privileges the attacker legitimately holds by design, such as a holder of `ROOT_PERMISSION`, a compromised admin key, or a proposal that passes according to the DAO's own rules. **If a proposal or account can obtain or exercise permissions beyond what it was granted, that is in scope.**
- Vulnerabilities in third-party dependencies (for example OpenZeppelin), unless Aragon's use of them makes them exploitable. Please report those upstream.
- Front-running, MEV or timestamp manipulation inherent to the underlying chain, unless they lead to a concrete impact specific to our contracts
- Gas optimizations, code style and best-practice recommendations without a demonstrable security impact
- Issues that only affect unsupported or modified versions

Frontend, website, infrastructure and social engineering issues are not eligible for the smart contract bug bounty, but still elegible for bug bounty so report them to [sirt@aragon.org](mailto:sirt@aragon.org).

## Rules of engagement

- Test only on local forks or testnets. Never test against mainnet deployments or live DAOs.
- Do not access, modify or move funds or data that are not yours, and do not exploit an issue beyond what is needed to demonstrate it.
- No denial-of-service, spam, phishing, social engineering or physical attacks against Aragon, its staff, its users or any DAO.
- Keep the details confidential until they are publicly disclosed as described below.

## Our commitments

| Stage | Target |
|---|---|
| Acknowledge your report | 2 business days (24 hours for urgent reports) |
| Initial severity assessment | 5 business days |
| Status updates | At least every 7 days until resolved |
| Credit | In the published advisory, unless you prefer to stay anonymous |

We assess severity based on impact and likelihood. If we disagree with your assessment, we will explain our reasoning.

## Coordinated disclosure

- We aim to fix critical issues as fast as possible, and all issues within 90 days.
- Aragon cannot upgrade deployed DAOs unilaterally: each DAO applies upgrades through its own governance. When deployed contracts are affected, we coordinate with affected DAOs, their security councils and other relevant parties before any public disclosure. This can extend the timeline beyond 90 days, and we will agree on a disclosure date with you.
- Please do not publish details (blog posts, talks, social media) before the advisory is published or the agreed date has passed.

## Safe harbor

If you act in good faith and follow this policy, we consider your research authorized, and:

- We will not initiate or support legal action against you, including under anti-hacking laws.
- If a third party takes legal action against you for activities conducted under this policy, we will make it known that your actions were authorized by us.
- We waive any restrictions in our terms of service that would otherwise prohibit research done in line with this policy.

We cannot authorize testing of systems we do not own, such as third-party protocols or contracts controlled by individual DAOs. If you are unsure whether an action is covered, contact us before proceeding.

## Bug bounty

Eligible reports may be rewarded under our bug bounty program. Reward amounts, eligibility, KYC and payment terms are defined there. If the bounty terms and this policy conflict, the bounty terms govern rewards and this policy governs disclosure.

## Audits

Releases of Aragon OSx and its official plugins are reviewed by independent security firms before deployment. Audits reduce risk but cannot eliminate it, which is why we run this program.

## Contact

- Email: [sirt@aragon.org](mailto:sirt@aragon.org)

*Last updated: [2026-10-30]*
