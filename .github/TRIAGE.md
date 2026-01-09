# Issue Triage Guidelines

This document provides guidelines for triaging issues in the Honeymelon support repository.

## Triage Process Overview

Triage is the process of reviewing new issues, verifying their validity, categorizing them, and prioritizing them for action. The goal is to ensure issues are properly labeled, contain necessary information, and are ready for the team to work on.

## Triage Workflow

### 1. Initial Review (Within 48 Hours)

When a new issue is created:

1. **Verify completeness**: Check that all required fields are filled out
2. **Check for duplicates**: Search for similar existing issues
3. **Validate information**: Ensure system info, versions, and steps are clear
4. **Apply initial labels**: Add type, status, and any relevant platform labels

### 2. Classification

#### Type Labels (Required)

Apply one primary type label:

- `bug` - Something isn't working as expected
- `enhancement` - New feature or improvement request
- `question` - Request for information or clarification
- `documentation` - Documentation improvements
- `feedback` - General feedback about the app

#### Status Labels (Required)

Apply appropriate status label:

- `status: needs-triage` - Default for new issues (auto-applied)
- `status: needs-info` - Missing critical information
- `status: confirmed` - Verified and ready to work on
- `status: in-progress` - Actively being worked on
- `status: blocked` - Cannot proceed (explain why in comment)
- `status: stale` - No activity for extended period

#### Priority Labels (For Bugs and Enhancements)

Assess priority based on impact and urgency:

- `priority: critical` - **Immediate attention required**
  - App crashes or force quits
  - Data loss or corruption
  - Security vulnerabilities
  - Complete feature breakage affecting all users
  - License validation failures preventing app use

- `priority: high` - **Significant impact**
  - Major feature not working for many users
  - Serious performance degradation
  - Installation or update failures
  - Regression from previous version
  - Widely-requested features

- `priority: medium` - **Moderate impact**
  - Feature works but has issues for some users
  - Minor performance issues
  - UI/UX issues affecting usability
  - Non-critical bugs with workarounds
  - Standard feature requests

- `priority: low` - **Minor impact**
  - Cosmetic issues
  - Edge case bugs
  - Nice-to-have features
  - Documentation improvements
  - Minor enhancements

### 3. Platform and Environment Labels

#### macOS Version Labels

Apply if issue is specific to a macOS version:

- `macos-version: sequoia` - macOS 15
- `macos-version: sonoma` - macOS 14
- `macos-version: ventura` - macOS 13
- `macos-version: monterey` - macOS 12

#### Chip Architecture Labels

Apply if issue is specific to processor type:

- `chip: apple-silicon` - M1/M2/M3/M4 Macs only
- `chip: intel` - Intel Macs only

### 4. Category Labels

Apply additional category labels as relevant:

- `crash` - App crashes or force quits
- `performance` - Slow, laggy, or resource-heavy
- `ui/ux` - User interface or experience issues
- `regression` - Previously worked, now broken
- `installation` - Install, update, or uninstall issues
- `integration` - Issues with system features or other apps
- `accessibility` - Accessibility or VoiceOver issues
- `localization` - Translation or language issues
- `security` - Security-related (public issues only)
- `license` - License, activation, or purchase issues

### 5. Special Labels

- `duplicate` - Mark as duplicate and link to original issue
- `wontfix` - Won't be addressed (explain reasoning)
- `invalid` - Not a valid issue or needs clarification
- `needs-reproduction` - Cannot reproduce, needs more details
- `good-first-issue` - Suitable for newcomers
- `help-wanted` - Community help welcomed

## Response Templates

### Need More Information

```markdown
Thank you for reporting this issue! To help us investigate, we need some additional information:

- [ ] [Specific information needed]
- [ ] [Other details required]

Please update your issue with this information when you have a chance.

I'm adding the `status: needs-info` label until we receive these details.
```

### Cannot Reproduce

```markdown
Thank you for the report! I'm unable to reproduce this issue with the information provided.

Could you please provide:
- More detailed steps to reproduce
- Any specific files or data involved
- Screenshots or screen recording
- Console logs (from Console.app, filtered for "Honeymelon")

This will help us track down the issue. Adding `needs-reproduction` label.
```

### Duplicate Issue

```markdown
Thank you for the report! This appears to be a duplicate of #[issue number].

I'm closing this in favor of the original issue. Please follow that issue for updates and feel free to add any additional information there.
```

### Confirmed Bug

```markdown
Thank you for the detailed report! I've confirmed this is a bug and have labeled it accordingly.

- **Priority**: [Critical/High/Medium/Low]
- **Affects**: [macOS versions, chip types]
- **Workaround**: [If any exists]

We'll investigate and work on a fix. I'll update this issue with progress.
```

### Feature Request Acknowledgment

```markdown
Thank you for the feature request! This is an interesting idea.

I've labeled this as an enhancement and [priority level] priority. We'll review this with the team and consider it for future releases.

Feel free to add any additional context or use cases that might help us better understand the request.
```

### Won't Fix

```markdown
Thank you for the suggestion/report. After careful consideration, we've decided not to pursue this because:

[Clear explanation of reasoning]

If circumstances change or you have additional information that might change our assessment, please let us know.
```

## Triage Checklists

### Bug Report Triage

- [ ] Reporter provided app version
- [ ] Reporter provided macOS version and build
- [ ] Reporter provided chip type (Apple Silicon/Intel)
- [ ] Reporter provided installation method
- [ ] Reproduction steps are clear and detailed
- [ ] Expected vs. actual behavior is described
- [ ] Logs or diagnostics included (if applicable)
- [ ] Checked for duplicates
- [ ] Applied type label (`bug`)
- [ ] Applied priority label
- [ ] Applied status label
- [ ] Applied platform labels (if specific)
- [ ] Applied category labels (if relevant)
- [ ] Left initial comment acknowledging the report

### Feature Request Triage

- [ ] Problem statement is clear
- [ ] Proposed solution is described
- [ ] Use cases are provided
- [ ] Checked for duplicates
- [ ] Applied type label (`enhancement`)
- [ ] Applied priority label (if applicable)
- [ ] Applied status label
- [ ] Applied category labels (if relevant)
- [ ] Left initial comment acknowledging the request

## Priority Guidelines by Category

### Critical Priority Scenarios

Always mark as `priority: critical`:

- App crashes on launch for all users
- Data loss or corruption
- Security vulnerabilities
- Complete inability to use paid features
- License validation failures

### High Priority Scenarios

Typically mark as `priority: high`:

- Feature completely broken for subset of users
- Severe performance degradation
- Regressions from stable versions
- Installation/update failures
- Major UI bugs blocking workflows

### Medium Priority Scenarios

Typically mark as `priority: medium`:

- Feature works but has issues
- Moderate performance issues
- UI/UX improvements
- Non-critical bugs with workarounds
- Well-justified feature requests

### Low Priority Scenarios

Typically mark as `priority: low`:

- Cosmetic issues
- Edge case bugs
- Minor enhancements
- Documentation updates
- Polish and refinements

## Special Cases

### License Issues

Issues involving licensing or activation:

1. Add `license` label
2. **Never** ask for actual license keys in public issues
3. May need to redirect to private support channel
4. Verify purchase method (Mac App Store, website, etc.)
5. Priority depends on whether user can use app or not

### Security Issues

For security issues reported publicly:

1. Add `security` label
2. **Immediately** close public issue if it's a genuine vulnerability
3. Request reporter use private security advisory
4. Follow security policy guidelines
5. Never discuss vulnerability details publicly

### Stale Issues

For issues with no activity:

1. Add `status: stale` label after 60 days of inactivity
2. Comment asking for update or confirmation still relevant
3. Close after 14 additional days if no response
4. Can be reopened if reporter returns with information

### Version-Specific Issues

When issue is specific to macOS version or chip:

1. Add appropriate platform labels
2. Try to reproduce on reported platform
3. Check if issue exists on other platforms
4. Note in comments which platforms are affected

## Triage Meeting Agenda

Weekly triage meetings should cover:

1. **New Issues** - Review all `status: needs-triage` issues
2. **Needs Info** - Follow up on `status: needs-info` issues
3. **Blocked Issues** - Review `status: blocked` to see if unblocked
4. **Stale Issues** - Address old issues with no activity
5. **High Priority** - Ensure critical/high priority issues are being addressed
6. **Feedback** - Review process improvements

## Tips for Effective Triage

1. **Be prompt**: Try to triage new issues within 48 hours
2. **Be respectful**: Always thank reporters and use friendly tone
3. **Be clear**: Explain reasoning behind labels and decisions
4. **Be helpful**: Provide workarounds when possible
5. **Be thorough**: Don't rush, ensure proper categorization
6. **Be consistent**: Use labels consistently across similar issues
7. **Be organized**: Keep issues well-documented and linked
8. **Be proactive**: Ask clarifying questions early

## Metrics to Track

- Time to first response
- Time to triage completion
- Number of issues in each status
- Number of critical/high priority open issues
- Duplicate rate
- Issues closed vs. opened per week
- Average resolution time by priority

## Tools and Resources

- [GitHub Labels Configuration](.github/labels.json)
- [Support Guidelines](../SUPPORT.md)
- [Contributing Guidelines](../CONTRIBUTING.md)
- [Security Policy](../SECURITY.md)

---

**Remember**: The goal of triage is to ensure every issue is acknowledged, properly categorized, and set up for success. Quality triage leads to better issue resolution and happier users! 🍈
