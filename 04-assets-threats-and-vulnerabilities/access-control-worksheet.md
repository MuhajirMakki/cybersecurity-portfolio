# Access Controls Worksheet

## Incident Summary

A payroll event was added to the system on 10/03/2023. The event was associated with the `Legal\Administrator` user and the computer `Up2-NoGud`. The IP address recorded in the event log was `152.207.255.255`.

## Control

**Authorization / Authentication**

## Note(s)

* The event took place on 10/03/2023 at 8:29:57 AM.
* The user was `Legal\Administrator` and the IP address was `152.207.255.255`.

## Issue(s)

* Robert Taylor Jr. was a contractor with administrator access.
* His contract ended in 2019, but his account was still able to access the payroll system in 2023.

## Recommendation(s)

* User accounts should expire after a defined period of time or when an employee or contractor leaves the organization.
* Contractors should have limited access to business resources based on their job responsibilities.
* Enable multi-factor authentication (MFA) for important business accounts.

## Analysis

The incident may have involved a former employee or a compromised account. The available information does not confirm who actually performed the activity, but the active account of a former contractor is a serious access control problem.

## Conclusion

This activity showed how unused or excessive user access can create security risks. Regularly reviewing accounts, limiting permissions, disabling inactive accounts, and using MFA can help prevent unauthorized access to business systems.
