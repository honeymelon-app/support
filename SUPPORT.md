# Support Guidelines

Thank you for using Honeymelon! This document explains how to get help with issues, questions, or feature requests.

## Getting Help

### Before Opening an Issue

1. **Search existing issues**: Check if your question or problem has already been reported
2. **Check discussions**: Browse our [community discussions](../../discussions) for solutions
3. **Review documentation**: Make sure you've read any relevant guides

### How to Get Support

#### For Bugs and Technical Issues

If you've found a bug or technical issue:

1. [Open a bug report](../../issues/new?template=bug_report.yml)
2. Fill out all required fields in the issue template
3. Include the following information:
   - macOS version (e.g., macOS 14.2 Sonoma)
   - Chip type (Apple Silicon M1/M2/M3/M4 or Intel)
   - Honeymelon app version
   - Installation method (Mac App Store, TestFlight, Direct Download, etc.)
   - Detailed steps to reproduce the issue
   - Expected vs. actual behavior
   - Relevant logs or diagnostic information
   - Screenshots or screen recordings if applicable

#### For Feature Requests

If you have an idea for a new feature:

1. [Open a feature request](../../issues/new?template=feature_request.yml)
2. Describe the problem your feature would solve
3. Explain your proposed solution
4. Provide any relevant examples or mockups

#### For Questions and Discussions

For general questions, ideas, or community discussions:

1. Visit our [Discussions](../../discussions) section
2. Choose the appropriate category
3. Search for existing discussions before creating a new one

### What Information to Include

When reporting issues, always include:

- **macOS Version**: Run `sw_vers` in Terminal or check System Settings > General > About
- **Chip Type**: System Settings > General > About > Chip (or `uname -m` in Terminal)
- **App Version**: Find this in Honeymelon's About window or Settings
- **Installation Method**: How you installed Honeymelon
- **Logs**: Any relevant console logs or crash reports
- **License Status**: Whether you're using a trial, free version, or licensed version

### Response Time

- **Critical bugs**: We aim to respond within 24-48 hours
- **Standard issues**: We aim to respond within 1 week
- **Feature requests**: May take longer to evaluate and prioritize
- **Discussions**: Community-driven; responses vary

### What NOT to Include

❌ **Never** include in public issues:
- License keys or activation codes
- Personal identifying information
- Credit card or payment information
- Private API keys or tokens
- Passwords or authentication credentials

For sensitive information, see our [Security Policy](SECURITY.md).

## Getting Diagnostic Information

### macOS System Information

```bash
# Get macOS version
sw_vers

# Get chip architecture
uname -m

# Get hardware info
system_profiler SPHardwareDataType
```

### Console Logs

To get relevant logs:

1. Open **Console.app**
2. Select your Mac in the sidebar
3. Filter for "Honeymelon"
4. Copy relevant log entries

### Crash Reports

If Honeymelon crashes:

1. Open **Console.app**
2. Go to **Crash Reports** in the sidebar
3. Look for recent Honeymelon crash reports
4. Attach the crash report to your issue

## License and Billing Issues

For issues related to:
- License activation
- Purchase problems
- Billing questions
- Subscription management

Please include in your issue:
- Order ID or receipt number (redact personal details)
- Purchase date
- Purchase platform (Mac App Store, website, etc.)
- Description of the problem

**Do NOT share your actual license key publicly.**

## Community Guidelines

When participating in this repository:

1. Be respectful and constructive
2. Follow our [Code of Conduct](CODE_OF_CONDUCT.md)
3. Stay on topic
4. Avoid duplicate issues
5. Provide clear, detailed information

## Issue Lifecycle

1. **New**: Issue has been created
2. **Triaged**: Team has reviewed and labeled the issue
3. **In Progress**: Someone is actively working on it
4. **Resolved**: Fixed in a release
5. **Closed**: Completed, duplicate, or not reproducible

## Additional Resources

- [Contributing Guidelines](CONTRIBUTING.md)
- [Security Policy](SECURITY.md)
- [Code of Conduct](CODE_OF_CONDUCT.md)
- [License](LICENSE)

Thank you for being part of the Honeymelon community! 🍈
