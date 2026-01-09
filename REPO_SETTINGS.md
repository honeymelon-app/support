# Repository Settings Guide

This document outlines the recommended settings for the Honeymelon support repository.

## Required Repository Settings

The following settings should be configured in the GitHub repository:

### General Settings

**Repository Name**: `support`

**Description**: 
```
🍈 Support, bug reports, feature requests, and community discussions for the Honeymelon macOS app
```

**Website**: [Your Honeymelon website URL if applicable]

**Topics/Tags**: 
- `macos`
- `support`
- `bug-reports`
- `feature-requests`
- `honeymelon`

**Features**:
- ✅ **Issues** - ENABLED (required for bug reports and feature requests)
- ✅ **Discussions** - ENABLED (required for community Q&A and conversations)
- ❌ **Projects** - Optional (enable if you want to track work)
- ❌ **Wiki** - Disabled (documentation in repo files instead)
- ❌ **Sponsorships** - Optional (enable if you have sponsorship tiers)

### Issues Configuration

**Issue Templates**: Already configured in `.github/ISSUE_TEMPLATE/`
- Bug report template (`bug_report.yml`)
- Feature request template (`feature_request.yml`)
- Template chooser config (`config.yml`)

**Labels**: Import from `.github/labels.json`

To import labels, use GitHub CLI:
```bash
# First, delete default labels (optional)
gh label list --json name --jq '.[].name' | xargs -I {} gh label delete {} --yes

# Import custom labels
cat .github/labels.json | jq -r '.[] | [.name, .description, .color] | @tsv' | \
  while IFS=$'\t' read -r name description color; do
    gh label create "$name" --description "$description" --color "$color" || true
  done
```

Or manually import via: Settings > Labels > Import labels

### Discussions Configuration

**Enable Discussions**: Yes

**Recommended Categories**:
1. **Announcements** 📢
   - Description: Official announcements about Honeymelon
   - Format: Announcement (only maintainers can post)

2. **General** 💬
   - Description: General discussions about Honeymelon
   - Format: Discussion

3. **Help & Support** 🙋
   - Description: Get help with using Honeymelon
   - Format: Q&A (can mark answers)

4. **Ideas** 💡
   - Description: Share ideas for new features
   - Format: Discussion

5. **Show and Tell** 🎨
   - Description: Show off your Honeymelon workflows and setups
   - Format: Discussion

6. **Feedback** 📝
   - Description: General feedback about the app
   - Format: Discussion

### Security

**Security Policy**: Configured in `SECURITY.md`

**Private Vulnerability Reporting**: 
- Enable in Settings > Security > Code security and analysis
- Enable "Private vulnerability reporting"

### Merge Settings

**Pull Requests** (if applicable):
- Allow merge commits: ✅
- Allow squash merging: ✅
- Allow rebase merging: ✅

### Branch Protection (if applicable)

For `main` branch:
- Require pull request reviews: Optional for support repo
- Require status checks: Not applicable (no code)

## Automation Options

### Recommended GitHub Actions

Consider setting up:

1. **Stale Issue Management**
   - Auto-label issues with no activity
   - Auto-close after extended inactivity

2. **Label Sync**
   - Keep labels in sync with `.github/labels.json`

3. **Issue Templates Validation**
   - Ensure required fields are filled

4. **Auto-labeling**
   - Auto-apply labels based on issue content

### Community Health Files

Already configured:
- ✅ README.md
- ✅ CODE_OF_CONDUCT.md
- ✅ CONTRIBUTING.md
- ✅ SECURITY.md
- ✅ SUPPORT.md
- ✅ LICENSE
- ✅ Issue templates
- ✅ .gitignore

## Access and Permissions

### Collaborators

**Recommended Team Structure**:
- **Maintainers**: Full access (Admin)
- **Triagers**: Triage access (can label, close, assign)
- **Community Moderators**: Write access for discussions

### Triage Access

Consider granting triage role to trusted community members:
- Can label issues
- Can close/reopen issues
- Can assign issues
- Cannot merge PRs or change settings

## Notification Settings

**For Maintainers**:
- Watch repository: All activity
- Enable notifications for:
  - New issues
  - New discussions
  - Security alerts
  - @mentions

**For Community**:
- Encourage subscribing to issues they're interested in
- Use issue labels to filter notifications

## Repository Insights

**Pulse**: Review weekly to track:
- New issues opened/closed
- Most active discussions
- Contributor activity

**Community Standards**: Should show:
- ✅ Code of conduct
- ✅ Contributing guidelines
- ✅ License
- ✅ README
- ✅ Security policy
- ✅ Issue templates

## API and Integrations

**Recommended Integrations**:
- GitHub Mobile app (for on-the-go triage)
- GitHub CLI (`gh`) for command-line management
- Slack/Discord bot (if you have community channels)

## How to Apply These Settings

### Via GitHub Web Interface

1. Go to repository Settings
2. Navigate through each section
3. Enable/configure as described above

### Via GitHub CLI

```bash
# Enable Issues
gh repo edit --enable-issues

# Enable Discussions
gh repo edit --enable-discussions

# Update description
gh repo edit --description "🍈 Support, bug reports, feature requests, and community discussions for the Honeymelon macOS app"

# Add topics
gh repo edit --add-topic "macos,support,bug-reports,feature-requests,honeymelon"
```

### Via GitHub API

```bash
# Update repository settings
curl -X PATCH \
  -H "Accept: application/vnd.github+json" \
  -H "Authorization: Bearer YOUR_TOKEN" \
  https://api.github.com/repos/honeymelon-app/support \
  -d '{
    "has_issues": true,
    "has_discussions": true,
    "has_wiki": false
  }'
```

## Post-Setup Checklist

After configuring the repository:

- [ ] Issues are enabled
- [ ] Discussions are enabled and categories created
- [ ] Labels imported from `.github/labels.json`
- [ ] Issue templates appear when creating new issue
- [ ] Security policy is visible
- [ ] All community health files are present
- [ ] Repository description and topics are set
- [ ] Private vulnerability reporting is enabled
- [ ] Team members have appropriate permissions
- [ ] Notification settings configured for maintainers

## Maintenance

**Monthly**:
- Review and update labels if needed
- Check issue template effectiveness
- Review stale issues
- Update documentation as needed

**Quarterly**:
- Review triage guidelines
- Assess label usage and consistency
- Update macOS version labels for new releases
- Review and update community health files

**Annually**:
- Complete review of all settings
- Update any outdated information
- Review security policy
- Assess community health and engagement

## Support and Questions

For questions about these settings or suggestions for improvements, please open a discussion in the repository.

---

**Note**: This repository contains no application code. It is solely for community support, issue tracking, and discussions about the Honeymelon macOS app.
