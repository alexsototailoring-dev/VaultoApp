# Context-Based Navigation Testing Notes

## Date: January 9, 2026

### Implementation Summary

The context-based navigation with Personal, Employer, and Advisor tabs has been successfully implemented.

### Tab 1 - Personal (Default)

**Banner**: "You're in control" with lock icon
- Text: "This is your personal insurance dashboard. All information is managed by you."
- Color: Primary green background

**Content**:
- Stats cards (Total Insured Value, Active Policies, Life Insurance Total)
- Coverage breakdown chart
- Policy cards with full CRUD functionality
- Search and filter capabilities

### Tab 2 - Employer

**Banner**: "Employer-provided benefits (read-only)" with building icon
- Text: "Insurance shown here is provided through your employment and is for reference only."
- Secondary: "Coverage may change if your employment status changes."
- Color: Amber/yellow background

**Content**:
- Employer cards showing Edinburgh Financial Services Ltd
- Employment period: Mar 2020 – Present
- Associated Insurance/Benefits displayed
- HR Contact information section

### Tab 3 - Advisor

**Banner**: "User-authorised, read-only access" with eye icon
- Text: "Advisors can only view information you choose to share. Vaulto does not provide advice."
- Color: Blue background

**Content**:
- Advisor cards showing John Smith
- Firm: Smith & Partners • Financial Advisor
- Jurisdiction: FCA Regulated, UK
- Contact details displayed

### Feature Flags Implemented

All future features are gated behind feature flags (all set to false):
- advisor_invite_enabled
- advisor_login_enabled
- employer_portal_enabled
- employer_share_enabled
- sharing_controls_enabled

### Compliance Language Verified

All banners use approved language:
- "read-only"
- "user-authorised"
- "for reference only"
- "Vaulto does not provide advice"

No prohibited language found (collaborate, manage together, advisor workspace, etc.)

### All Tests Passed
