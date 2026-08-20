---
title: RCL VC for WOrkforce Development
description: The objective of this document is to provide a roadmap for the design and implementation of an online cloud-based platform for RCL Verifiable Credentials for Workforce Development.
parent: Introduction
nav_order: 1
---

# RCL Verifiable Credentials for Workforce Development
## A Roadmap for an Online Platform

Ray Consulting Limited

Version: A , 19/09/2025 

# Introduction

The objective of this document is to provide a roadmap for the design and implementation of an online cloud-based platform for RCL Verifiable Credentials for Workforce Development.

# Purpose

The purpose of the online platform is to facilitate the communication and sharing of RCL Verifiable Credentials among issuers, holders and verifiers.

# What are RCL Verifiable Credentials

Verifiable Credentials (VCs) are tamper-proof, cryptographically secure digital credentials that can be instantly checked and validated. Standardized by the World Wide Web Consortium (W3C), they act as the digital equivalent of physical documents like education and training qualifications. Unlike static PDF documents, VCs contain built-in cryptographic signatures that allow anyone to verify their authenticity automatically without needing a central database. The RCL Verifiable Credential is a specific implementation of W3C Verifiable Credential standards.

# Pillars of the Online Platform

The following pillars underpin the design of the online platform:

## Digital

Credentials are machine-readable and cryptographically secured. The data model for the credential is standardized by the [W3C](https://www.w3.org/TR/vc-overview-1.0/). When issued to a holder, a credential can take the format of a PNG image file that contains the data for the credential embedded in the image file. Credentials will be digitally stored on the platform.

## Trust

The technology operates through an ecosystem containing three primary roles:

### Issuer
The authoritative entity  that creates the credential and digitally signs it using their private cryptographic key. An issuer issues a credential to a holder.

``Examples of Issuers``
- An education or training institution offering courses and certifications
- An organization managing the competences of its employees
- A product owner offering certification for users of its products
- Licensing or certification bodies regulating workers in an occupational area
- An industry group or committee ensuring competence of workers in their sector
- Apprenticeship providers who tracks the competences of apprentices
- Any organization developing and tracking the competences of workers


### Holder
The recipient who receives the credential from an issuer and safely stores it on a smartphone, computer or digital wallet.

``Examples of Holders``
- Learner
- Student
- Employee
- Any Individual


### Verifier
The third-party entity that reviews the holder's credential and uses the issuer's cryptographic public key to instantly check the credential's validity.

``Examples of Verifiers``
- Employers
- Organizations
- Licensing authorities
- Governments
- Any organization verifying competences of workers

### Internal Trust
The ecosystem relies on internal trust rather than external regulations. It operates as a closed-loop or peer-to-peer trust network. 

Verifiers, eg. employers, will trust a credential created by an issuer once they deem that the credential is relevant to a worker's job. For instance , a verifier will trust a credential in Database Administration if it deems that the credential provides the relevant competences to Database Administrators. 

The holder will trust the credential once it is endorsed by the employer as providing relevant skills and knowledge for the job duties that they perform.

In this way, the internal trust pyramid provides relevant credentials that are highly desired and trusted by the stakeholders: issuers, verifiers and holders.

## Stackable

### Modular

Credentials are modular and are issued to holders who demonstrate competence in a job area.

### Stand-alone

Each credential must be stand-alone. The credential must encompass all the competences to fulfil a job area and should not depend on other credentials to complete the job. For instance, a credential in Database Administration should be sufficient for a Database Administrator to carry out his/her duties. A credential that covers database backups only is insufficient, and the the credential will be deemed incomplete. A credential should ideally cover an entire job area. Credentials that are created from the subdivision of individual job duties  may be deemed insufficient.

### Learning Pathways

Credentials can be stacked or combined to provide a ``learning pathway`` for the learner. For instance, credentials in database, storage and compute can be stacked together to provide a learning pathway for a Cloud Administrator role. Issuers will provide recommended learning pathways to stack credentials that they create and issue. Holders can also stack credentials that they have earned to create their own learning pathways. The holders are free to design their own custom leaning pathways or use those recommended by issuers.

### Multi-source

Stand-alone credentials can be issued from various issuers. For instance, a credential on database can be issued from one issuer, another issuer can issue a credential on storage and a third issuer can issue a credential on compute. The holder should be able to seamlessly stack all  three credentials they earn from each issuer  to create their learning pathway.

## Competence-based

Credentials should provide the holder with the relevant competences (outcomes) to carry out their duties in a job area. A credential should not be time dependent but outcome dependent. A learner can take any amount of time to achieve the competences (outcomes) that underpin a credential.

## Sharable

Holders should be able to share their credentials online with verifiers such as employers. Verification of a credential will not need permission or a direct connection back to the original issuer.

# Platform Design

## Description

The RCL Verifiable Credential for Workforce Development will be a cloud-based platform to enable the communication and sharing of credentials among issuers, holders and verifiers. It will be offered free of charge. The platform will comprise the following modules:

## Issuer Module

### Issuer Details

An issuer will be able to display their organization's details such as name, logo, contacts, address, website, etc. on the platform. The issuer will also be able to upload their verification details.

### Credentials

The issuer will display the credentials that they create and offer to holders. Credentials will be organized by sector and occupational areas. Where applicable, online registration links for each credential can be included by the issuer to allow holders to register for a credential.

### Learning Pathways

An issuer will create and display learning pathways for their credentials. A learning pathway will outline how credentials can be stacked together to provide career routes for a learner.

## Holder Module

### Credentials

A holder will be able to upload credentials in the PNG image format and store them in the platform in a digital format. Credentials will be grouped into ``collections`` and shared with verifiers, such as employers.

### Learning Pathways

A holder will be able to stack their credentials together in a learning pathway. The pathway can be customized and be personal to the holder or they can be based on recommendations provided by an issuer. The holder will be able to share their learning pathways with verifiers.

## Verifier Module

### Shared Credentials

Holders will be able to share their credentials as collections with one or more verifiers. They can also share their stacked credentials as learning pathways. A verifier will use the platform to view and validate the credentials shared with them by the holders.

# Implementation Schedule

| Module          | Completion Date 
| --------------- | ---------------
| Issuer Module   | 30 Sep 2026 
| Holder Module   | 30 Oct 2026 
| Verifier Module | 30 Dec 2026 

# Reference Software Applications

The following reference software applications will form the technology ecosystem that supports the platform:

- RCL VC Issuer - A windows based application available free of charge in the [Windows Store](https://apps.microsoft.com/detail/9mw1q2kptsb2?hl=en-US&gl=TT) that allows an issuer to create and issuer verifiable credentials.

- RCL VC Trust Registry - An [Online Registry](https://trustregistry.vc.rclapp.com/) available for issuers to obtain obtain a validation that confirms they are who they claim to be.

- RCL VC Verifier - A mobile application available free of charge in the [Google Play](https://play.google.com/store/apps/details?id=com.rclapp.vcverifier&hl=en) store that allows a verifier to validate a credential by scanning the QR code contained in the credential.

- RCL VC Wallet - A mobile application available free of charge in the [Google Play](https://play.google.com/store/apps/details?id=com.rclapp.vcwallet&hl=en) store that allows holders to store their credentials in a digital wallet.

# Conclusion

This document outlined a design for an online platform for RCL Verifiable Credentials for Workforce Development. The platform will be offered free of charge to issuers, holders and verifiers of credentials to allow for communication and sharing of the credentials. A schedule was provided that outlined the projected date for delivery of the modules that comprise the platform. The pillars that underpin the platform design are as follows: digital, trust, stackable,  competence-based and sharable. The software applications that comprise the technology ecosystem that supports the platform were also identified.







