# 📧 O365 User Setup & Support Guide

**Created by:** Justin Asamoah  
**Last updated:** 2025-10-04

## Overview
Step-by-step support instructions for common Microsoft 365 (O365) user issues.

- Password resets with MFA (self-service & assisted)  
- OneDrive sync problems (reset & re-sign-in)  
- Outlook configuration (desktop & mobile)  
- Teams access & permissions  

---

## 1) Password Reset with MFA
### Self‑Service (User)
1. Go to `https://portal.office.com` → *Can’t access your account?* or `https://aka.ms/sspr`  
2. Enter work email and complete MFA  
3. Set a new password  
4. Sign back into Outlook, Teams, OneDrive

**Confirm:** User can access webmail & Teams.

### Assisted Reset (IT)
1. Verify identity per policy  
2. Reset in Entra ID / AD; enforce change at next sign-in  
3. Confirm Conditional Access/MFA as required  
4. User signs into webmail first, then desktop apps

> If still failing: clear Windows Credential Manager entries.

---

## 2) Outlook Configuration
**Desktop – Fix Sync / New Profile**  
1. Close Outlook → Control Panel → *Mail (Microsoft Outlook)* → *Show Profiles…*  
2. *Add…* → enter email → create new profile  
3. Set *Always use this profile* → open Outlook  
4. Test send/receive

**Mobile (iOS/Android)**  
1. Install Outlook app  
2. Add work email → complete MFA  
3. Enable notifications

---

## 3) OneDrive – Sync Problems
**Quick Checks**  
- Signed in with work account?  
- Internet/VPN ok?  
- Files On-Demand on?

**Full Reset**  
1. Quit OneDrive  
2. Run: `%localappdata%\Microsoft\OneDrive\onedrive.exe /reset`  
3. Start OneDrive and sign in  
4. Re-link SharePoint libraries (*Sync*)

**Confirm:** Green check marks; edits sync both ways.

---

## 4) Teams – Access & Permissions
**Membership & Guests**  
1. Confirm membership / invite guest  
2. Verify tenant allows guest access  
3. Sign out/in to refresh

**Client Fix (Desktop)**  
1. Sign out  
2. Clear cache: `%appdata%\Microsoft\Teams`  
3. Sign in and retest

---

## 5) Quick Triage Checklists
**Email/Outlook** – webmail test, license/mailbox check, new profile  
**OneDrive** – account sign-in, reset client, path/file size limits  
**Teams** – membership, try web client, SharePoint permissions

---

## 6) Communication Templates
**Password Reset – User Email**  
> I’ve reset your password. Please sign into https://portal.office.com, then Outlook/Teams. If prompts repeat, restart your device and try again.

**Outlook Sync – User Email**  
> We repaired your Outlook profile. Keep Outlook open a few minutes while it finishes syncing. If emails don’t appear, check webmail and reply here.

**OneDrive Reset – User Email**  
> After the OneDrive reset, please sign back in. Watch for the green check marks. Re-link any SharePoint libraries via the site’s *Sync* button.

---

## Appendix: Useful Shortcuts (Windows)
- Credential Manager (Control Panel)  
- Teams cache: `%appdata%\Microsoft\Teams`  
- OneDrive reset: `%localappdata%\Microsoft\OneDrive\onedrive.exe /reset`
