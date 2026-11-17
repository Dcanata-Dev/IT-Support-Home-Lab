# HD-002 — Account Lockout

**Status:** Resolved  
**Category:** Account Management  
**Environment:** Windows Server 2025 / Windows 11  
**Domain:** adlab.test

## Issue
Employee Alex Morgan (`amorgan`) was unable to sign in because the domain account had been locked after multiple unsuccessful login attempts.

## Troubleshooting and Resolution
1. Configured the Default Domain Policy with an account lockout threshold of 3 invalid attempts.
2. Set the account lockout duration to 15 minutes.
3. Set the reset account lockout counter to 15 minutes.
4. Disabled the policy allowing the built-in Administrator account to be locked out.
5. Refreshed Group Policy on the Windows 11 client.
6. Confirmed that Alex's account became locked after unsuccessful login attempts.
7. Opened Active Directory Users and Computers on the domain controller.
8. Located Alex Morgan under the Company Users organizational unit.
9. Selected the Unlock account option in the Account properties.
10. Confirmed that Alex could successfully sign in again.

## Verification
- Confirmed the client received the updated Group Policy.
- Confirmed Windows displayed the account-locked-out message.
- Manually unlocked Alex's account in Active Directory.
- Confirmed successful domain sign-in as `ADLAB\amorgan`.

## Outcome
Alex's account was successfully unlocked, and domain access was restored.

## Skills Practiced
- Group Policy Management
- Account lockout policies
- Active Directory Users and Computers
- Account status verification
- Unlocking domain user accounts
- Windows domain authentication
- Helpdesk troubleshooting and documentation
