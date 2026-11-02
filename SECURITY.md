# Security Policy

Aragon X AG maintains the Aragon OSx and aragonOS smart contract frameworks and their official plugins. These contracts govern and protect real assets held by DAOs, so we treat security reports as a top priority and value the work of researchers who help keep them safe.

This policy applies to the Aragon OSx and aragonOS smart contract frameworks and their official plugins maintained by Aragon. Other software and services maintained by Aragon may also be reported through the channels below. A repository’s presence under [github.com/aragon](https://github.com/aragon) does not by itself place it in scope: third-party forks, archived repositories and unrelated projects are excluded unless explicitly stated otherwise. If a repository publishes its own `SECURITY.md`, that policy takes precedence.

## Reporting a vulnerability

**Please do not open a public issue, pull request or discussion, and do not share details with third parties.**

Report privately through one of these channels:

1. **GitHub private vulnerability reporting (preferred):** on the affected repository, open the *Security* tab and click *Report a vulnerability*.
2. **Email:** [sirt@aragon.org](mailto:sirt@aragon.org).

### Active exploits and emergencies

If you believe a vulnerability is being actively exploited, or funds are at immediate risk:

- Email [sirt@aragon.org](mailto:sirt@aragon.org) with **`[URGENT]`** at the start of the subject line

Notify us immediately about active exploits or funds at immediate risk; a complete proof of concept can follow. Urgent reports are acknowledged within 24 hours.

### What to include

- Affected repository, contract(s) and version or commit hash
- Network and contract address, if deployed contracts are affected
- A description of the vulnerability and its root cause
- Smart contract reports must include a working, runnable proof of concept demonstrating the vulnerability and its impact in an isolated local environment, with instructions for reproducing it. Foundry or Hardhat tests are preferred.
- The impact: what an attacker can achieve, under which preconditions, and an estimate of funds at risk
- A suggested fix (optional)

### AI-assisted reports

We welcome findings discovered with the help of AI tools. Every report must still be reviewed and validated by a human before submission and meet the reporting requirements above. Speculative, unverified or bulk-generated reports will be closed without a detailed response, and repeated low-quality submissions may lead to exclusion from rewards.

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
- Projects and versions not currently maintained and explicitly supported by Aragon, including older versions and archived projects, unless expressly included. This exclusion applies even if they remain deployed.
- Issues introduced solely by third-party modifications, rather than by Aragon-maintained code

Frontend, website, infrastructure and social engineering issues are outside the smart contract scope described above, but reports may still be considered for rewards. Report them to [sirt@aragon.org](mailto:sirt@aragon.org).

## Rules of engagement

- Perform vulnerability testing and verification, including proof-of-concept execution, only in isolated local environments, such as local forks or private local test networks. Testing or verifying vulnerabilities on mainnet or public testnets is prohibited, including against contracts or DAOs you deploy or control. Do not broadcast exploit transactions to any public network.
- Do not access, modify or move real funds or private data that are not yours, and do not exploit an issue beyond what is needed to demonstrate it.
- Do not disrupt live contracts, DAOs, services or networks, including through denial-of-service or distributed denial-of-service attacks. Demonstrating a vulnerability that freezes funds, bricks a DAO or prevents governance execution is permitted in the isolated local environments described above.
- No spam, phishing, social engineering or physical attacks against Aragon, its staff, its users or any DAO.
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

- We aim to prepare fixes within 90 days, prioritizing critical vulnerabilities.
- Each DAO controls its own upgrades. We cannot identify or contact every deployment, so we coordinate privately with priority affected DAOs based on risk and our ability to reach them. We consider remediation complete for this process once those DAOs have upgraded. We then publish the fix and vulnerability details on a disclosure date agreed with the researcher. This coordination may extend beyond 90 days.
- Please do not publish details (blog posts, talks, social media) before the advisory is published or the agreed date has passed.

## Safe harbor

If you act in good faith and follow this policy, we consider your research authorized, and:

- We will not initiate or support legal action against you, including under anti-hacking laws.
- If a third party takes legal action against you for activities conducted under this policy, we will make it known that your actions were authorized by us.
- We waive any restrictions in our terms of service that would otherwise prohibit research done in line with this policy.

We cannot authorize testing of systems we do not own, such as third-party protocols or contracts controlled by individual DAOs. If you are unsure whether an action is covered, contact us before proceeding.

## Bug bounty and rewards

Aragon handles bug bounty reports through an internal review process. We assess each report individually and award payments for qualifying findings on a case-by-case basis. We do not publish a fixed reward schedule; eligibility, reward amounts and payment requirements are determined during review and communicated directly to the researcher. Submitting a report does not guarantee a reward.

## Audits

Releases of Aragon OSx and its official plugins are reviewed by independent security firms before deployment. Audits reduce risk but cannot eliminate it, which is why we welcome vulnerability reports from researchers.

## Contact

- Email: [sirt@aragon.org](mailto:sirt@aragon.org)

*Last updated: [2026-11-03]*
