# Security Policy

## Reporting a Vulnerability

The OPI security policy aims to efficiently handle security vulnerabilities
while minimizing public disclosure until a fix is available.

Reporters are requested to submit security issues privately via the
[GitHub advisory](https://github.com/opiproject/opi/security/advisories/new)
system.

Reports will be acknowledged within 5 calendar days. OPI maintainers will
respond to a report within a maximum of calendar 10 days, indicating the
next steps in handling the submission.

## Reporting a Vulnerability in 3rd Party Modules

The focus of this security policy is on reporting OPI security vulnerabilities.

Security issues in third-party modules should be reported according to their
own security policies or directly to their respective maintainers if no such
security policy is in place for the respective module.

## Vulnerability Disclosure Policy

Upon receiving a security report, OPI follows the Common Vulnerabilities and
Exposures (CVE®) process outlined below:

1. OPI maintainer acknowledges the receipt of the report and calls for a
maintainer/security experts meeting to discuss the scope and
assess the severity of the vulnerability using [CVSS score](https://nvd.nist.gov/vuln-metrics/cvss/v3-calculator)
as well as identify any potentially related problems.

2. OPI board is notified about the identified vulnerabilities and their severities.
Resources are identified and assigned to investigate the issue in more detail
so that a fix or workaround can be proposed.

3. The reporter is notified about the next steps in handling the vulnerability
and may be invited to collaborate on a fix.

4. Once a fix or workaround is prepared, it is submitted for a standard review
by creating a pull request (PR) *without disclosing any details about the
vulnerability* but merely stating what the patch does.

5. Once the PR(s) is merged, the most recent official release will be used as
a baseline for a maintenance release and will include only the fix(es)
identified for the issue at hand.

6. Once the maintenance release is tagged, the OPI maintainer will
[request a CVE](https://www.cve.org/ReportRequest/ReportRequestForNonCNAs#RequestCVEID) for the vulnerability.

7. After the issue has been disclosed, an announcement will be made on the OPI
Slack [#proj-security](https://opi-project.slack.com/archives/C05LU6KJ8KZ) channel
with more information about the issue and the fix so that community members can
decide for themselves what their exposure is and if they should move to the new
release.

## Comments on This Policy

If you have suggestions on how this process could be improved, please submit
a [pull request](https://github.com/opiproject/opi) or [file an issue](https://github.com/opiproject/opi/issues/new) to discuss.

---

By adopting this security policy, OPI aims to foster a secure and
collaborative environment for its open-source community. The process ensures
timely and responsible handling of security vulnerabilities, keeping the users'
interests in mind. Your cooperation and adherence to this policy are greatly
appreciated.

Please remember that security is a shared responsibility, and together, we can
enhance the safety of the OPI project for everyone.
