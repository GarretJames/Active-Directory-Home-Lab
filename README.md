# Active-Directory-Home-Lab
Windows Server Active Directory home lab demonstrating domain administration, Group Policy, DNS, role-based access control, help-desk workflows, and troubleshooting.
Project Overview

Designed and implemented a virtualized Active Directory environment to practice common enterprise IT administration and cybersecurity tasks.

The project focuses on centralized identity management, secure access to departmental resources, Windows domain authentication, and the principle of least privilege.

Technologies Used

Windows Server 2025

Windows 11 Enterprise Evaluation

VMware Workstation

Active Directory Domain Services (AD DS)

DNS and Group Policy

PowerShell

Windows SMB file sharing and NTFS permissions

Lab Environment

Component

Configuration

Domain

jameslab.test

Domain Controller

DC01 — 10.10.10.10

Windows Workstation

WS01 — 10.10.10.20

Virtual Network

VMnet2 (Host-only)

Network Subnet

10.10.10.0/24

The environment was built on an isolated virtual network for educational testing.

Implementation

1. Active Directory Administration

Configured a Windows Server domain controller.

Created organizational units, employee accounts, and security groups.

Organized accounts and groups for departmental administration.

Completed five simulated help-desk administration exercises.

2. Security Policy Configuration

Configured domain password policies.

Configured account lockout policies.

Used Group Policy to implement centralized security settings.

3. Departmental Access Control

Created shared folders for HR, Finance, IT, and Sales.

Configured security groups and file permissions using the AGDLP model:

Accounts → Global Groups → Domain Local Groups → Permissions

This structure supports centralized access management and least-privilege authorization.

4. Workstation Deployment

Installed a Windows 11 Enterprise Evaluation virtual machine.

Configured static IPv4 addressing and domain DNS.

Verified network connectivity with the domain controller.

Verified Active Directory DNS service discovery.

Successfully joined WS01 to jameslab.test.

Authenticated an employee using domain credentials.

Security Validation

Tested access controls using the HR employee account JAMESLAB\casey.wilson.

Test

Expected Result

Actual Result

Domain authentication

Successful sign-in

PASS

HR security group membership

HR groups present

PASS

HR shared-folder access

Access permitted

PASS

Create and save HR test file

Write permitted

PASS

Finance shared-folder access

Access denied

PASS

These tests confirm the expected behavior for the tested HR employee. Other departmental access scenarios were configured but were not comprehensively tested from WS01.

Screenshots and Evidence

Authorized HR Access



An authenticated HR employee successfully created and saved a document in the authorized HR share.

Unauthorized Finance Access



The same employee received a Windows permissions error when attempting to access the Finance share.

Skills Demonstrated

Windows Server administration

Active Directory identity management

Group Policy configuration

DNS and TCP/IP troubleshooting

Role-based access control

Least-privilege implementation

SMB and NTFS permission management

Domain-joined workstation deployment

Help-desk administration

Security testing and documentation

Key Takeaways

This project reinforced the importance of verifying security controls from the perspective of an actual user.

Successful configuration alone does not guarantee correct authorization. Testing both permitted and denied access provides stronger evidence that security policies are functioning as intended.

The lab also provided practical experience troubleshooting Windows permissions, virtual networking, and domain authentication.

Environment: Isolated educational home lab

Purpose: Cybersecurity education and professional portfolio development
