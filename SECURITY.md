# Security Policy

## Reporting Security Vulnerabilities

The Honeymelon team takes security vulnerabilities seriously. We appreciate your efforts to responsibly disclose your findings.

### How to Report a Security Vulnerability

**Please DO NOT report security vulnerabilities through public GitHub issues.**

Instead, please report security vulnerabilities by:

1. **Email**: Send details to `security@honeymelon.app` (if available)
2. **GitHub Security Advisory**: Use GitHub's [private vulnerability reporting](../../security/advisories/new)

### What to Include in Your Report

Please include as much of the following information as possible:

- Type of vulnerability (e.g., code execution, privilege escalation, data exposure)
- Full paths of affected source file(s)
- Location of the affected code (tag/branch/commit/direct URL)
- Step-by-step instructions to reproduce the vulnerability
- Proof-of-concept or exploit code (if possible)
- Impact of the vulnerability
- Your assessment of severity
- Any potential mitigations you've identified

### What to Expect

1. **Acknowledgment**: We'll acknowledge receipt of your report within 48 hours
2. **Assessment**: We'll investigate and assess the vulnerability
3. **Updates**: We'll keep you informed of our progress
4. **Resolution**: We'll work on a fix and coordinate disclosure timing with you
5. **Credit**: With your permission, we'll credit you in the security advisory

### Response Timeline

- **Initial Response**: Within 48 hours
- **Status Update**: Within 7 days
- **Resolution Timeline**: Varies by severity
  - Critical: As soon as possible
  - High: Within 30 days
  - Medium: Within 60 days
  - Low: Within 90 days

## Supported Versions

We provide security updates for the following versions:

| Version | Supported          |
| ------- | ------------------ |
| Latest  | ✅ Yes             |
| < Latest| ⚠️ Best effort     |

We recommend always using the latest version of Honeymelon for the best security.

## Security Best Practices for Users

### Safe Installation

- Download Honeymelon only from official sources:
  - Mac App Store
  - Official Honeymelon website
  - Official TestFlight builds
- Verify the app is properly signed by checking in System Settings > Privacy & Security

### Permissions

Honeymelon may request the following macOS permissions:
- **Accessibility**: For productivity features
- **Screen Recording**: For capturing workflows
- **File System Access**: For managing documents
- **Notifications**: For reminders and alerts

Review and grant only the permissions you're comfortable with.

### License Key Security

- **Never share your license key publicly** (GitHub issues, forums, social media)
- Store your license key securely
- If you believe your license key is compromised, contact support immediately

### Data Privacy

- Honeymelon processes data locally on your Mac
- Review our Privacy Policy for details on data handling
- Regularly backup your data
- Use macOS FileVault for encryption at rest

## Security Features in Honeymelon

- **Sandboxing**: App Store version runs in Apple's App Sandbox
- **Code Signing**: All releases are properly signed
- **Notarization**: All releases are notarized by Apple
- **Secure Updates**: Updates are delivered over HTTPS
- **Local Processing**: Your data stays on your Mac

## Known Security Considerations

### macOS Permissions

Honeymelon requires certain macOS permissions to function. These permissions are:
- Clearly disclosed during first launch
- Used only for stated purposes
- Minimal and necessary for functionality

### Third-Party Dependencies

Honeymelon may use third-party libraries and frameworks. We:
- Regularly review dependencies for vulnerabilities
- Update dependencies promptly when security issues are discovered
- Use only well-maintained, reputable libraries

## Scope

### In Scope

Security vulnerabilities in:
- The Honeymelon macOS application
- Official distribution channels
- This support repository (if containing sensitive data)

### Out of Scope

- Social engineering attacks
- Physical access to unlocked devices
- Issues in deprecated versions
- Third-party integrations not directly controlled by Honeymelon
- Theoretical vulnerabilities without practical exploit

## Safe Harbor

We support safe harbor for security researchers who:

- Make a good faith effort to avoid privacy violations and disruption
- Act for the sole purpose of improving security
- Don't exploit vulnerabilities beyond the minimum necessary for demonstration
- Give us reasonable time to address issues before public disclosure
- Comply with all applicable laws

## Recognition

We appreciate the security research community and will:

- Credit researchers who report valid vulnerabilities (with permission)
- Maintain a security acknowledgments section for contributors
- Consider participating in security researcher recognition programs

## Security Updates

Security updates will be:
- Released as soon as practical after validation
- Announced through standard release channels
- Detailed in release notes (after users have had time to update)

## Questions

For questions about this security policy, please open a discussion in the [Discussions](../../discussions) section (for non-sensitive questions) or contact us privately for security-related inquiries.

## Policy Updates

This security policy may be updated from time to time. Check back regularly for changes.

---

**Thank you for helping keep Honeymelon and our users safe!** 🍈🔒
