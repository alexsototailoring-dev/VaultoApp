# Vaulto - Insurance FinTech App TODO

## Authentication & User Management
- [x] Secure Sign-Up/Sign-In via Manus OAuth
- [x] User profile with Net Worth field
- [x] User profile with Primary Location field

## Insurance Dashboard
- [x] Policy cards displaying Provider Name, Policy Type, Policy Number, Premium Amount, Renewal Date
- [x] Days Until Renewal countdown on each card
- [x] Total Insured Value counter at top of dashboard

## Document Vault & Data Entry
- [x] Upload PDF/Photo feature for policy documents
- [x] Manual entry form with Provider, Policy #, Renewal Date, Premium fields
- [x] Policy coverage amount field for Total Insured Value calculation

## Wealth Intelligence
- [x] Logic: If Life Insurance value > £250,000, show Wealth Insight notification
- [x] Notification: "Strategic Alert: Your asset profile qualifies for an Offshore Trust review. Protect your legacy from inheritance tax."

## Stripe Subscription Integration
- [x] Stripe integration setup
- [x] Vaulto Pro subscription plan at £3.99/month
- [x] Dashboard view-only mode until subscription is active

## UI/UX
- [x] Landing page with fintech aesthetic
- [x] Blue/white/slate color palette
- [x] Modern, high-trust design
- [x] Responsive layout

## Database
- [x] Users table with profile fields (netWorth, primaryLocation)
- [x] Policies table with all required fields
- [x] Policy documents table for file storage references

## Bug Fixes
- [x] Fix Stripe payment checkout flow not working (tested and working)
- [x] Fix subscription status not updating in frontend after payment
- [x] Remove Wealth Insight notification from dashboard (user request)
- [x] Update landing page copy to focus on protection rather than wealth management
- [x] Add UK insurer logos/names section (Scottish Widows, Aviva, Legal & General, etc.)
- [x] Add testimonial section with sample user quote
- [x] Update pricing copy - change "Wealth Intelligence alerts" to "Smart renewal reminders"
- [x] Add custom Vaulto logo to navigation, footer, and favicon
- [x] Add FAQ section with common questions
- [x] Add "How it works" 3-step visual guide
- [x] Add social proof stats section
- [x] Update headline from "Your Insurance Policies, One Dashboard" to "Insurance Made Simple"
- [x] Fix Profile page to use custom Vaulto logo instead of shield icon (also fixed Subscription page)
- [x] Add Terms & Privacy links to footer
- [x] Add contact/support section with email
- [x] Add animated counters for social proof stats

## Production Readiness
- [x] Create Terms of Service page
- [x] Create Privacy Policy page
- [x] Create Cookie Policy page
- [x] Add coverage breakdown chart to dashboard
- [x] Add search and filter for policies
- [x] Add policy edit functionality
- [x] Add policy delete functionality
- [x] Improve empty states when no policies exist
- [x] Add better loading states and skeletons
- [x] Add proper error handling throughout
- [x] Update Profile page wording (remove wealth references)
- [x] Add onboarding flow for new users
- [x] Mobile optimization and polish

## Compliance Updates (Regulatory Safety)
- [x] Remove all unverifiable metrics (500+, £2M+, 98%, 4.9★)
- [x] Remove insurer logos and implied partnerships
- [x] Remove testimonials and savings claims
- [x] Update hero copy to neutral language
- [x] Update features to remove emotive/protective language
- [x] Update pricing to remove advisory-sounding language
- [x] Update contact info to Edinburgh
- [x] Add legal disclaimer to footer
- [x] Add disclaimer to dashboard totals
- [x] Change hero headline back to "Insurance Made Simple"

## Brand Redesign (Calm, Established, Infrastructure-like)
- [x] Update CSS with new color palette (Deep Forest Green, Parchment Off-White, Muted Gold)
- [x] Remove all gradients
- [x] Update primary buttons to Deep Forest Green
- [x] Update backgrounds to Parchment Off-White (#F9F7F2)
- [x] Update text colors (Espresso Black #121212, Warm Grey)
- [x] Use Muted Gold (#B08D57) only for logo/badges
- [x] Update all copy to neutral tone (View, Store, Access, Track, Organise)
- [x] Remove emotional/persuasive language
- [x] Ensure WCAG AA contrast compliance
- [x] Add metallic brushed gold background to navigation header

## Advisor & Employer Pages (Non-Advised Coordination)
- [x] Create advisors table in database schema
- [x] Create employers table in database schema
- [x] Create advisor documents table
- [x] Create employer documents table
- [x] Create tRPC routers for advisors CRUD
- [x] Create tRPC routers for employers CRUD
- [x] Build Advisors page with Name, Firm, Role, Jurisdiction, Contact, Notes, Documents
- [x] Build Employers page with Name, Period, Benefits, Documents, HR Contact
- [x] Add required disclaimers to both pages
- [x] Add Pro tier gating for multiple advisors/employers
- [x] Add navigation links to dashboard
- [x] Write tests for new features

## Context-Based Navigation (Personal / Employer / Advisor Tabs)
- [x] Create top-level persistent navigation tabs: Personal, Employer, Advisor
- [x] Personal tab: Add "You're in control" banner with lock icon
- [x] Personal tab: Set as default dashboard view
- [x] Employer tab: Add "Employer-provided benefits (read-only)" banner
- [x] Employer tab: Add empty state with "No employer benefits added" message
- [x] Employer tab: Add "Add employer benefit" CTA (feature-flagged)
- [x] Advisor tab: Add "User-authorised, read-only access" banner (never dismissible)
- [x] Advisor tab: Add empty state with "No advisors added" message
- [x] Advisor tab: Add "Add advisor details" and "Invite advisor" CTAs (feature-flagged)
- [x] Add feature flags: advisor_invite_enabled, advisor_login_enabled, employer_portal_enabled, employer_share_enabled
- [x] Ensure all language is compliance-safe (read-only, user-authorised, for reference only)
- [x] Remove any advisory/selling language

## Pricing, Early Access & Building Vaulto Update

### Pricing Tiers
- [x] Update Free tier: 1 policy limit (was unlimited for Pro)
- [x] Add Early Access tier: 2 policies, invite-only
- [x] Update Pro tier: 10 policy limit (not unlimited)
- [x] Add annual pricing: £29.99/year (recommended) alongside £3.99/month
- [x] Update subscription page with new copy (verbatim from spec)
- [ ] Implement paywall logic for Free→Pro, Early Access→Pro, Pro limit reached

### Early Access Invite System
- [x] Add Early Access flag to user model
- [x] Create invite system: each Early Access user can invite up to 3 people
- [x] Add Profile → Early Access section with invite button
- [x] Create invite confirmation dialog with checkbox
- [x] Set up invite acceptance page
- [x] No counters, no gamification, no rewards

### Building Vaulto Page
- [x] Create /building-vaulto page with 4 sections
- [x] Section 1: Current stage (Private early access)
- [x] Section 2: What's next (planned milestones)
- [x] Section 3: How Vaulto is funded (self-funded)
- [x] Section 4: Industry conversations (exploratory)
- [x] Add mandatory footer disclaimer
- [x] Add subtle homepage footnote link "What's next for Vaulto"
- [x] Add footer link "Building Vaulto"

### Pro Features to Implement
- [x] Renewal reminders (email) - 30/14/7 days before (UI added, backend cron job pending)
- [x] Emergency / Quick Access view
- [ ] PDF export (policy summary)
- [ ] Document OCR (auto-detect, user must verify)
- [ ] Read-only sharing with family members


## Backend Enforcement & Pro Features

### Policy Limit Enforcement (Backend)
- [x] Add policy limit check in policies.create mutation
- [x] Return clear error message when limit exceeded
- [x] Check user tier (Free: 1, Early Access: 2, Pro: 10)
- [x] Write tests for policy limit enforcement

### PDF Export
- [x] Create PDF generation (client-side with jsPDF)
- [x] Include all policies with key details
- [x] Include user profile info
- [x] Add compliance disclaimer to PDF
- [x] Add "Export PDF" button to dashboard (Pro only)
- [x] Write tests for PDF export

### Renewal Reminder Cron Job
- [x] Create cron job endpoint for renewal reminders
- [x] Query policies with upcoming renewals
- [x] Check reminder preferences (30/14/7 days)
- [x] Send notifications via built-in notification API
- [x] Track last reminder sent to avoid duplicates
- [x] Write tests for reminder logic


## Advanced Pro Features

### Scheduled Cron Job for Renewal Reminders
- [x] Create scheduled task to run daily at 9am UK time
- [x] Call the processRenewalReminders endpoint automatically
- [x] Add logging for cron job execution (already in renewalReminders.ts)

### Document OCR for Policy Extraction
- [x] Create OCR endpoint using LLM vision capabilities
- [x] Extract policy fields: provider, policy number, premium, coverage, renewal date
- [x] Add "Scan Document" button to Add Policy dialog (Pro only)
- [x] Show extracted fields for user verification before saving
- [x] Write tests for OCR extraction

### Family Sharing (Emergency Page)
- [x] Create family_shares table in database
- [x] Generate unique shareable links for Emergency page
- [x] Create public /share/:token route for read-only access
- [x] Add Family Sharing section to Emergency page (Pro only)
- [x] Allow users to revoke/regenerate share links
- [x] Write tests for family sharing


## Bug Fixes

### Payment/Upgrade Not Working
- [x] Investigate Stripe checkout flow
- [x] Fix payment button functionality (changed window.open to window.location.href)
- [x] Test upgrade process


## Master Prompt Feature Refinements

### 1. Renewal Reminders Refinements
- [x] Update email copy to use exact verbatim text from spec
- [x] Per-policy toggle available in Add Policy dialog
- [x] Pro feature badge shown
- [x] Default to 30 + 7 days (changeable)
- [x] Removed urgency language

### 2. Emergency Card Refinements
- [x] Mobile-first design (minimal taps, max 2)
- [x] Add emergency/claims phone number field to policies
- [x] Add user notes display
- [x] Implement offline caching for emergency card
- [x] Removed guidance text

### 3. PDF Export Refinements
- [x] Minimal black & white design (no charts, no interpretation)
- [x] Add mandatory footer disclaimer
- [x] Include user name, date generated
- [x] No logos beyond Vaulto

### 4. Family Sharing Refinements
- [x] Add scope selection (all policies OR selected only)
- [x] Add duration options (7, 30, 90, 180, 365 days)
- [x] Default to 90 days
- [x] Add confirmation checkbox with exact copy
- [x] Add read-only banner for viewers (never dismissible)
- [x] Downloads controlled by allowDownloads flag

### 5. OCR Refinements
- [x] Update UI copy to "Detected from document — please verify."
- [x] Ensure fields are editable and require user confirmation
- [x] Remove any confidence scores or "we think" language
- [x] Never auto-save silently


## Bug Fix: Free Tier Policy Creation
- [x] Investigate why free tier users cannot add policies
- [x] Fix policy creation flow for free tier (should allow 1 policy)
- [x] Test free tier policy creation


## Bug Fix: Add Policy Dialog Error on Published Site
- [x] Investigate JavaScript error when clicking Add Policy
- [x] Fix the error causing "An unexpected error occurred" (SelectItem empty value)
- [ ] Test on published site after republishing


## Header Styling Update
- [x] Remove white rectangle background from logo (make circular/rounded-full)
- [x] Change "Vaulto" text from white to dark green (#2D4A3E)


## OCR Cost Optimization

### File Hash Caching
- [x] Create document_scans table to track scans
- [x] Store file hash, extracted data, and timestamp
- [x] Check hash before calling API - return cached result if exists
- [x] Cache expires after 30 days

### Monthly Scan Limits
- [x] Track scans per user per month
- [x] Pro users: 20 scans/month limit
- [x] Show friendly message when limit reached
- [x] Reset count on 1st of each month

### System Prompt Refinement
- [x] Update prompt for UK insurance specificity
- [x] Add claimsPhone field extraction
- [x] Add premiumFrequency field


## UX Improvements (Pre-Launch Polish)

### Claims Phone UI Enhancement
- [x] Add "Claims/Emergency Phone" field to Add Policy dialog below Policy Number
- [x] Use tel: link for tap-to-call on policy view
- [x] Add UK phone formatting placeholder (03xx xxx xxxx or 0800 xxx xxxx)
- [x] Display claims phone prominently on policy cards

### Free Tier Edit/Delete Access
- [x] Allow free users to edit their single policy
- [x] Allow free users to delete their single policy
- [x] Show "Limit Reached" upgrade prompt when adding second policy
- [x] Highlight Pro features in upgrade prompt (10 policies, OCR scan, etc.)

### GDPR Data Export (ICO Compliance)
- [x] Add "Privacy & Data" section to Profile page
- [x] Create "Download My Data" button
- [x] Export user profile data (name, email)
- [x] Export all policy data (provider, policy #, expiry, claims phone)
- [x] Provide both JSON and CSV download options


## Additional Features (Pre-Launch Final)

### Tesseract.js Local OCR Fallback
- [x] Install tesseract.js package
- [x] Create local OCR component for free tier users
- [x] Extract basic text from policy documents
- [x] Parse extracted text for policy fields (provider, policy number, dates)
- [x] Show "Basic scan" label for free tier vs "AI-powered scan" for Pro
- [x] Reserve LLM-based OCR for Pro users only

### Account Deletion (GDPR Compliance)
- [x] Add "Delete My Account" button to Profile page
- [x] Create confirmation dialog with checkbox acknowledgment
- [x] Implement 30-day grace period before permanent deletion
- [x] Add account_deletion_requested_at field to users table
- [x] Create backend endpoint for account deletion request
- [x] Show countdown/status for pending deletions
- [x] Allow cancellation during grace period

### Emergency View Policy Icons
- [x] Add policy type icons (car, home, life, health, travel) to Emergency page
- [x] Make icons visually prominent for quick scanning
- [x] Add color-coded badges for each policy type
- [x] Ensure icons match Dashboard styling for consistency


## Premium Payment Reminder Feature (Pro)

### Database & Backend
- [x] Add premium_due_date field to policies table
- [x] Add reminder_enabled boolean field
- [x] Add reminder_schedule field (7_days_before, 3_days_before, due_date)
- [x] Add missed_payment_warning_enabled boolean field
- [x] Create backend endpoints for updating premium reminder settings

### UI Integration
- [x] Add "Premium & Reminders" section to policy detail view
- [x] Create premium due date input with date picker
- [x] Add reminder toggle controls (7 days, 3 days, due date)
- [x] Add missed payment warning toggle
- [x] Show next reminder date clearly
- [x] Gate feature behind Pro subscription

### OCR Integration
- [x] Update OCR extraction to detect premium due dates
- [x] Add user confirmation step for OCR-extracted dates
- [x] Allow editing of extracted dates before saving

### Compliance & Safety
- [x] Use neutral, non-advised language in all notifications
- [x] Do not imply guarantees or enforcement
- [x] Keep feature read-only (no payment triggers)


## Email Notifications & Dashboard Enhancements

### Email Notification Delivery
- [x] Add email notification preferences to user settings
- [x] Create opt-in/opt-out toggle for premium reminders
- [x] Connect to built-in notification API for email delivery
- [x] Send reminder emails at scheduled times (7 days, 3 days, due date)
- [x] Send missed payment warning emails

### Payments Due Dashboard Widget
- [x] Create "Payments Due" widget component
- [x] Show upcoming premium payments across all policies
- [x] Display due dates, amounts, and policy names
- [x] Sort by nearest due date first
- [x] Add to main dashboard view

### Recurring Payment Detection
- [x] Detect monthly vs annual premium frequency
- [x] Auto-suggest next due date after payment confirmation
- [x] Calculate next due date based on premium frequency
- [x] Pre-fill suggested date for user confirmation


## Onboarding Tour

### Tour Component
- [x] Create OnboardingTour component with step navigation
- [x] Design visually appealing tour modal/overlay
- [x] Add progress indicator (step 1 of 3, etc.)
- [x] Include skip and next buttons

### Tour Steps
- [x] Step 1: Add your first policy (highlight Add Policy button)
- [x] Step 2: Scan documents with OCR (explain Pro feature)
- [x] Step 3: Emergency quick access (show Emergency page)

### Tour Integration
- [x] Track tour completion in user preferences
- [x] Show tour automatically for new users
- [x] Add "Restart Tour" option in settings
- [x] Persist completion status in database


## Admin Dashboard & Founder's Pass System

### Database Schema
- [x] Create founder_passes table (code, type, duration, maxUses, usedCount, isRevoked, createdAt)
- [x] Create pass_redemptions table (passId, userId, redeemedAt)
- [x] Add indexes for efficient lookups

### Backend API
- [x] Create admin-only middleware/guard
- [x] Add createPass endpoint
- [x] Add listPasses endpoint with usage stats
- [x] Add revokePass endpoint
- [x] Add listRedemptions endpoint
- [x] Add getAnalytics endpoint (totals, rates)
- [x] Add redeemPass endpoint for users

### Admin Dashboard UI (/admin)
- [x] Role-based access control (admin only)
- [x] Create Pass tab with form (type, duration, maxUses)
- [x] All Passes tab with table and revoke buttons
- [x] Redemptions tab showing user redemption history
- [x] Analytics section (total passes, redemptions, active codes, rate)

### User Redemption Flow
- [x] Add redeem pass page/modal
- [x] Validate pass code
- [x] Apply subscription benefits on redemption
- [x] Show success/error feedback


## Admin Analytics Dashboard (Compliance-Safe)

### System Overview
- [x] Display total users count
- [x] Display total policies stored
- [x] Display total active Pro users
- [x] Display total policies with reminders enabled

### Premium Reminder Analytics (Aggregated Only)
- [x] Number of premium reminders sent (by period)
- [x] % of policies with reminders enabled
- [x] % of premiums marked as confirmed before due date
- [x] % of premiums overdue after due date
- [x] Reminder effectiveness comparison (with vs without)

### Event-Based Metrics (Anonymous)
- [x] Create analytics_events table for anonymous event tracking
- [x] Track reminder_sent events
- [x] Track payment_confirmed events
- [x] Track premium_overdue_warning_sent events
- [x] Store with day-level timestamps only

### Trends & Insights
- [x] Reminder adoption over time chart
- [x] Overdue rate trend (weekly/monthly)
- [x] Confirmation timing distribution chart

### UI Requirements
- [x] Clean, neutral admin styling
- [x] "Aggregated data only" labels
- [x] Charts and summary cards (not tables)
- [x] No raw data export


## Bug Fixes

- [ ] Fix /admin route 404 error on published site
- [x] Replace generic shield icon with Vaulto logo on loading screen
- [x] Replace generic shield icon with Vaulto logo in "No policies yet" section
- [x] Change Upgrade to Pro buttons to gold colour (matching hero header)
- [x] Fix Upgrade to Pro button text visibility (dark text on gold background)
- [x] Revert Upgrade buttons back to original green colour (user request)
- [x] Update Admin page to use email whitelist instead of database role

## Admin Dashboard Polish

- [x] Update "Confirmed Before Due" to "Payment Confirmed Before Due (User-Reported)"
- [x] Add footer disclaimer to Admin Analytics page


## Batch Code Generation

- [x] Add backend endpoint for batch code creation
- [x] Create batch generation UI form with prefix pattern and count
- [x] Display generated codes with copy-all functionality


## Courtesy Access Rename

- [x] Replace "Founder's Pass" with "Courtesy Access" in Admin UI
- [x] Replace "Partner" terminology with neutral language
- [x] Set COURTESY as default code prefix


## Batch Code Generation

- [x] Add backend endpoint for batch code creation
- [x] Create batch generation UI form with prefix pattern and count
- [x] Display generated codes with copy-all functionality

## Stripe Integration Review

- [x] Review current Stripe setup and configuration
- [x] Verify subscription flow works correctly
- [x] Check webhook handling for payment events


## Sentry Error Monitoring Integration

- [x] Install Sentry packages for React and Node.js
- [x] Request Sentry DSN from user
- [x] Configure Sentry on frontend (React error boundary)
- [x] Configure Sentry on backend (Express middleware)
- [x] Add environment and release tracking

## Tour Styling Updates
- [x] Replace shield crest with Vaulto logo in onboarding tour
- [x] Add golden gradient background to Welcome to Vaulto header in tour
- [x] Fix mobile header layout - Vaulto text and Pro badge overlapping on portrait mode
- [x] Keep Vaulto text visible on mobile while preventing overlap with Pro badge
- [x] Add annual Pro tier (£29.99/year) to landing page pricing section
- [x] Auto-redirect to Dashboard after successful login
- [x] Remove Annual Pro tier - keep only Monthly Pro
- [x] Add privacy and data protection messaging (footer and sign-up)
- [x] Create desktop-friendly landing view for unauthenticated users in app
- [x] Add Annual Pro tier back to app pricing (web/app only)
- [x] Add Sign In and Set Up Account CTAs to landing view
- [x] Ensure authenticated users redirect to Dashboard
- [ ] Remove Test Mode card from Subscription page
- [ ] Investigate and fix email notification system for reminders
- [ ] Add AI Document Scanning feature card to features grid
- [ ] Add What's Next for Vaulto card section above footer
- [ ] Add Founder's Statement section with Edinburgh background
- [ ] Remove Test Mode card from Subscription page
- [x] Fix Sign In button delay - render immediately without waiting for auth state
- [x] Create distinct /signup and /login routes in the app
- [x] Update Set Up Account CTA to route to /signup
- [x] Update Sign In CTA to route to /login
- [x] Remove Annual Pro tier from app Home page pricing (keep only Free and Monthly)
- [x] Remove What's Next for Vaulto card from app Home page
- [x] Remove Founder's Statement section from app Home page

## Bug Fixes - January 14, 2026

- [ ] Fix OAuth redirect URI error on app.vaultoapp.com ("Permission denied - Redirect URI is not set")

- [x] Fix SEO: Add keywords meta tag to homepage
- [x] Fix SEO: Optimize title length (30-60 characters)
- [x] Fix SEO: Add meta description (50-160 characters)
- [x] Add canonical URL meta tag for SEO
- [x] Create sitemap.xml for search engine indexing
- [x] Create robots.txt with sitemap reference

## AWS Migration - January 14, 2026

- [x] Create comprehensive AWS migration guide
- [x] Prepare codebase for standalone deployment
- [x] Replace Manus OAuth with AWS Cognito or custom JWT auth
- [x] Create Docker configuration for containerization
- [x] Create AWS deployment scripts
- [x] Document environment variables and secrets setup
- [x] Create database migration guide (to RDS PostgreSQL)

## Bug Fixes - January 14, 2026 (continued)

- [ ] Fix authentication issue caused by recent change

## Founder's Pass UX - January 17, 2026

- [x] Create pre-redemption popup banner for Founder's Pass discovery
- [x] Create post-redemption confirmation popup banner
- [x] Integrate banners into dashboard with proper state management
- [x] Ensure banners don't show after redemption is complete

## Email Integration - January 21, 2026

- [ ] Install Resend SDK for email delivery
- [ ] Create email service module with send function
- [ ] Create HTML email template for renewal reminders
- [ ] Update renewal reminders to send emails directly to users
- [ ] Request and configure RESEND_API_KEY
- [ ] Test email delivery


## Soft Launch Feedback - January 21, 2026

- [x] Add "No expiry / Rolling contract" option for policies without fixed end dates
- [x] Add support for multiple cover types (e.g., Life Cover + Serious Illness Cover as separate amounts)
- [x] Fix OCR to auto-fill claims phone number when detected
- [x] Improve OCR date recognition to avoid picking up letter header dates as expiry dates

## Bank-Grade Security - January 21, 2026

- [ ] Research bank-grade security standards (PCI DSS, SOC 2, ISO 27001)
- [ ] Implement security headers (CSP, HSTS, X-Frame-Options, etc.)
- [ ] Add encryption indicators and trust badges throughout the app
- [ ] Create dedicated Security page explaining all protections
- [ ] Add security messaging to homepage and marketing
- [ ] Implement audit logging for sensitive operations
- [ ] Add "Your data never leaves your control" messaging


## Bank-Grade Security - January 2026

- [x] Add bank-grade security headers to server (HSTS, X-Frame-Options, CSP, etc.)
- [x] Create SecurityBadge component with trust signals
- [x] Add SecurityShield indicator to dashboard
- [x] Create dedicated /security page explaining all protections
- [x] Add Security link to homepage footer

## Session Security - January 2026

- [x] Disable persistent login sessions (changed from 1 year to 8 hours)
- [x] Require re-authentication on browser close (session-only cookies without maxAge)

## Samsung/Android Compatibility - January 2026

- [x] Investigate Samsung/Android browser compatibility issues
- [x] Implement device detection for Android devices (useDeviceDetect hook)
- [x] Add Android-specific CSS fixes (scroll lock, viewport, touch, flexbox, modals)
- [x] Update viewport meta tag for better Android compatibility

## Multi-File Document Upload - January 2026

- [ ] Add PDF file support to document scanner
- [ ] Implement multiple image upload for multi-page documents
- [ ] Update AI extraction to combine data from multiple pages/files
- [ ] Update UI to show upload progress for multiple files

## Multi-File Document Upload - January 2026

- [x] Add PDF file support to document scanner (pdfjs-dist)
- [x] Implement multiple image upload for multi-page documents
- [x] Update AI extraction to combine data from multiple pages (mergeExtractedData)
- [x] Create MultiFileScanDocument component with drag-and-drop support
- [x] Add file preview thumbnails with navigation
- [x] Support up to 20MB files

## File Type Icons - January 2026

- [x] Add PDF icon overlay on PDF file thumbnails (red badge with page count)
- [x] Add image icon overlay on image file thumbnails (blue badge)

## App-Level PIN & Biometric Authentication - January 2026

- [ ] Add PIN hash field to users table in database
- [ ] Create PIN setup flow for new users
- [ ] Create PIN verification screen after OAuth login
- [ ] Implement biometric authentication (Face ID/Touch ID) using WebAuthn API
- [ ] Allow users to choose PIN, biometric, or both
- [ ] Add PIN/biometric settings to Profile page
- [ ] Store biometric credentials securely


## App-Level PIN/Biometric Security
- [x] Add PIN setup flow (4-6 digit PIN)
- [x] Add PIN verification screen after OAuth login
- [x] Add biometric authentication support (Face ID/Touch ID via WebAuthn)
- [x] Store PIN securely (hashed) in database
- [x] Add "Forgot PIN" recovery flow
- [x] Add PIN/biometric settings in Profile page
- [x] Prevent automatic dashboard access from saved OAuth accounts
- [x] Write tests for PIN security features

## PIN Setup Mandatory
- [x] Remove "Skip for now" option from PIN setup screen
- [x] Make PIN setup required before accessing protected pages

## Auto-Lock & PIN Strength
- [x] Add auto-lock timeout after 15 minutes of inactivity
- [x] Track user activity (mouse, keyboard, touch events)
- [x] Clear PIN verification and require re-entry after timeout
- [x] Add PIN strength indicator during setup
- [x] Show visual feedback for 4-digit vs 6-digit PINs
- [x] Encourage stronger 6-digit PINs

## Security Enhancements
- [x] Add configurable auto-lock timeout (5/15/30 minutes)
- [x] Store user's preferred timeout in database
- [x] Add timeout selector in Profile settings
- [x] Add email-based PIN recovery flow
- [x] Generate and send PIN reset codes via email
- [x] Create PIN reset verification page
- [x] Add security activity log table
- [x] Track PIN verification attempts
- [x] Track biometric usage
- [x] Create security activity log UI in Profile

## Security Feature Card - January 2026

- [x] Add security feature card to Home page features section
- [x] Highlight bank-grade security (PIN, biometric, encryption)
- [x] Use appropriate security messaging

## Security Page & Trusted Devices - January 2026

- [x] Create dedicated Security page with detailed security information
- [x] Add navigation link to Security page from Home and Profile
- [x] Explain PIN protection, biometrics, auto-lock, encryption
- [x] Add trusted devices database table
- [x] Create API routes for managing trusted devices
- [x] Add "Remember this device" checkbox in PIN verification
- [x] Store device fingerprint and allow skipping PIN on trusted devices
- [x] Add trusted devices management in Profile settings

## Navigation Logo Link - January 2026

- [x] Make logo in navigation header clickable to go to home page

## Bug Fix - Login Page Responsiveness - January 2026

- [x] Investigate OAuth login page responsiveness issue
- [x] Check if recent changes affected the OAuth redirect
- [x] Fix PinGate/PIN verification screen not rendering on mobile

## Bug Fix - PIN Verification Auto-Submit - January 2026

- [x] Fix PIN verification auto-submitting after 4 digits
- [x] Store PIN length when setting up and use it for verification
- [x] Only auto-submit when full PIN length is entered

## Bug Fix - PIN Verification UI - January 2026

- [x] Show all 6 PIN input slots regardless of PIN length
- [x] Add explicit submit button instead of auto-submit
- [x] Remove dependency on stored PIN length for verification UI

## Bug Fix - Biometric Button Visibility - January 2026

- [x] Hide biometric button when device doesn't support biometrics
- [x] Check platform authenticator availability before showing button

## Bug Fix - iOS Safari Modal Stuck - January 2026

- [x] Fix Add Policy modal getting stuck on iOS Safari
- [x] Enable scrolling inside modal on mobile
- [x] Ensure close button is accessible

## Chrome iOS Biometric Support - January 2026

- [x] Investigate why Face ID works in Safari but not Chrome on iOS
- [x] Check WebAuthn platform authenticator detection for Chrome iOS
- [x] Behavior is correct: Safari shows Face ID, Chrome hides it (not supported)

## AI Scan Feature Improvements - January 2026

- [x] Fix multiple file selection on mobile (added Add More button)
- [x] Add "Add More" button to allow adding files one at a time
- [x] Add clearer messaging about supported document types (images, PDFs)
- [x] Improve mobile-friendly upload experience

## Camera Capture & Scan History - January 2026

- [x] Add dedicated "Take Photo" button for camera capture on mobile
- [x] Use capture="environment" attribute for back camera
- [x] Add scan history database table
- [x] Create API routes for saving and retrieving scan history
- [x] Create scan history UI component showing recent scans
- [x] Allow users to re-use extracted data from previous scans

## PDF Document Support for AI Scan - February 2026

- [x] Update file input to accept PDF documents (application/pdf)
- [x] Add PDF processing logic for AI scan recognition
- [x] Convert PDF pages to images for AI analysis
- [x] Update UI to show PDF files in the upload list
- [x] Fix PDF file selection on Samsung Internet browser (added .pdf extension)
- [x] Updated UI to clearly show PDF support
