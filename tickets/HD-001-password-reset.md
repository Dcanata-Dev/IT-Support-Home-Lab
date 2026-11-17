# HD-001 — Password Reset

**Status:** Resolved  
**Category:** Account Management  
**Environment:** Windows Server 2025 / Active Directory  
**Domain:** adlab.test

## Issue
Employee Alex Morgan (`amorgan`) reported being unable to sign in because he had forgotten his password.

## Troubleshooting and Resolution
1. Opened Active Directory Users and Computers.
2. Located Alex Morgan under the Company Users organizational unit.
3. Selected Reset Password.
4. Assigned a new temporary password.
5. Enabled "User must change password at next logon."
6. Confirmed that the password reset completed successfully.

## Verification
- Confirmed the account was not disabled.
- Confirmed the account was not locked out.
- Confirmed that a password change is required at the next logon.

## Outcome
Password reset completed successfully. The account remains enabled and requires the employee to establish a new password at the next sign-in.

## Skills Practiced
- Active Directory Users and Computers
- Locating domain user accounts
- Resetting user passwords
- Configuring account options
- Verifying account status
