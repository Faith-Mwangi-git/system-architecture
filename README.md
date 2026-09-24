# Smart Attendance System

A secure, mobile app-based attendance management platform that helps lecturers create and monitor attendance sessions while allowing students to confirm attendance through QR codes, biometric, facial verification or scanning student id.


1. Overview

<!-- The Smart Attendance System replaces manual attendance registers with a centralised digital platform. Lecturers can manage units, allocate students, create attendance sessions, display or download session QR codes, and review attendance reports. Students can register, join their allocated units, verify their identity, scan a session QR code, confirm attendance, and monitor their attendance history and academic progress. -->

2. Objectives

1. Provide secure registration and sign-in for lecturers and students.
2. Allow lecturers to manage units and their allocated students.
3. Enable lecturers to create attendance sessions and generate unique QR codes.
4. Allow students to record attendance by scanning a valid QR code,biometric, facial verification or scan student id.
6. Prevent duplicate, expired, or unauthorised attendance submissions.
7. Provide attendance history, reports, and progress summaries.
8. Reduce paperwork and improve the reliability of institutional attendance records.

 3. User Roles

3.1 Lecturer

Lecturers are responsible for managing teaching units and attendance sessions.

#### Registration

Lecturer registration requires:

- Full name
- Email address
- Staff number
- Password

The system should validate that the email address and staff number are unique. Email verification and approval by an administrator are recommended before the account becomes active.

#### Sign-in

Lecturers sign in using:

- Staff number or registered email address
- Password

#### Lecturer Features

- View and update their profile.
- Add and manage teaching units.
- View students allocated to each unit.
- Create, open, pause, and close attendance sessions.
- Generate, display, refresh, and download a session QR code.
- Set session rules such as duration, attendance window, and verification method.
- View live attendance as students check in.
- Correct an attendance record with an auditable reason, subject to permission.
- View attendance reports by unit, session, student, date range, or attendance status.
- Export reports in CSV or PDF format.

### 3.2 Student

Students use the system to verify their identity, record attendance, and track progress.

#### Registration

Student registration requires:

- Full name
- Registration number
- Email address
- Student id
- Password

The system should validate that the email address and registration number are unique. Student records should be linked to an approved institutional or unit allocation record where possible.

#### Sign-in

Students sign in using:

- Email address
- Password

#### Student Features

- View and update their profile.
- View allocated units.
- Scan an active attendance QR code.
- Complete biometric,scanning id or facial verification when enabled.
- Confirm attendance for a valid session.
- View attendance history and attendance reports.
- View unit-level attendance percentages and progress summaries.
- Review rejected or incomplete attendance attempts and the reason for rejection.

### 3.3 Administrator 

An administrator role is recommended for institutional control,

- Approve lecturer accounts and manage user status.
- Create or import units and student allocations.
- Assign lecturers to units.
- Manage system-wide settings and attendance policies.
- Review audit logs and resolve disputes.

## 4. Functional Requirements

### 4.1 Authentication and account management

- Users must register according to their role.
- Users must sign in using valid credentials.
- Passwords must be stored as secure hashes and must never be stored as plain text.
- Users must be able to sign out securely.
- The system should support password reset through a verified email address.
- The system should enforce account status checks such as pending, active, suspended, or deactivated.
- Repeated failed sign-in attempts should be rate-limited.

## 6. Core Modules

### Authentication module

Handles registration, sign-in, sign-out, password reset, email verification, role checks, and account status.

### User and profile module

Stores lecturer and student profiles, registration numbers, staff numbers, contact details, and profile status.

### Unit and allocation module

Manages units, academic periods, lecturer assignments, student allocations, and membership status.

### Attendance session module

Creates sessions, controls session state, applies time windows, and generates signed QR tokens.

### Verification module

Performs QR validation,scanning id, biometric and facial verification, where legally and operationally approved.

### Reporting module

Calculates attendance summaries, provides filtering and exports, and exposes student progress information.

### Notification module

Optionally sends email or in-app notifications for account verification, password reset, session events, and attendance issues.

## 13. Enhancements

- Administrator dashboard and approval workflows.
- Bulk import of students, lecturers, units, and allocations.
- Multi-factor authentication.
- Offline attendance capture with synchronisation and conflict handling.
- Geofencing or classroom network validation, subject to privacy review.
- Notifications for low attendance and missed sessions.
- Calendar integration for scheduled classes.
- Analytics for attendance trends and at-risk students.
- Native mobile applications with secure device registration.

## Conclusion
The Smart Attendance System should provide a dependable attendance record without making classroom check-in unnecessarily difficult. QR, biometric,scanning id and facial verification attendance offers a fast primary workflow. Clear permissions, auditable changes, privacy controls, and consistent reporting are essential to making the system suitable for real academic use.
