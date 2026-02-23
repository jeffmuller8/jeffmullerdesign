---
layout: project
title: FX Payment System
description: Unifying a fragmented FX payment ecosystem into a single experience
category: Finance
project_date: 2022-2024
client: Financial Services
role: Sr UX Designer
image: /assets/images/portfolio/fxpayments/hero.jpg
hover_image: /assets/images/portfolio/fxpayments/images/Grouped Payments.png
password_protected: true
password: jeffmullerdesign!1
---

## Summary

An FX payments platform that leverages across three separate systems—pricing, settlement, and reconciliation—making multi-currency payments.

I led the UX design of a unified FX payment application that consolidated funding sources, beneficiaries, pricing, settlement, approvals, and audit visibility into a single experience—balancing novice usability with trader-level sophistication.

The project evolved over two years in an agile, shifting environment with expanding scope, regulatory considerations, and technical constraints.

---

## The Problem

Executing an FX payment required navigating multiple systems:

1. One system to initiate funding
2. Another to retrieve live FX pricing
3. A third to settle and reconcile the trade
4. Later, a fourth system to analyze performance

For novice users (treasury, accounts payable), this fragmentation created confusion and operational risk.
For experienced FX traders, flexibility and precision were non-negotiable.

The organization needed:
- A single interface
- Access to all funding accounts and beneficiaries
- Real-time FX pricing
- Approval workflows
- Settlement coordination
- Regulatory audit visibility

But underneath, the systems remained separate.

---

## Phase 0: Selling the Vision

Before engineering began, I was asked to design a high-fidelity prototype that simulated integration across systems.

The goal was not to build it immediately—it was to create something believable enough to secure stakeholder buy-in.

I designed a cohesive, modern interface that:
- Unified funding sources and beneficiaries
- Displayed FX pricing inline
- Modeled trade execution and settlement flows
- Reduced cross-system mental switching

The prototype successfully aligned leadership and unlocked development investment.

<div class="project-gallery">
    <div class="gallery-grid">
        <div class="gallery-item">
            <img src="/assets/images/portfolio/fxpayments/images/Original Concept.png" alt="Original FX payment concept design">
            <p class="gallery-caption">A visually pleasing payments solution to help sell the vision</p>
        </div>
    </div>
</div>

---

## Designing the Unified Flow

The core payment flow required users to:

- Select the funding account (including currency and balance)
- Select a beneficiary (account, SWIFT, currency)
- Choose settlement date
- Retrieve live FX pricing
- Confirm and submit for approval

Under the hood:
- Pricing was retrieved from a separate FX system
- Settlement occurred in another system
- Reconciliation synced back to the funding source
- Analysis tools were layered in later

The challenge was to make this feel like one coherent action.

---

## Designing for Dual User Types

This system had to serve:

**Novice Users**
- Accounts payable
- Treasury staff
- Occasional FX users

They needed:
- Clarity
- Guardrails
- Reduced error risk
- Simplified mental models

**Experienced Traders**
- Expected control
- Expected precision
- Needed access to rate timing and settlement nuance

The interface had to abstract complexity without removing power.

<div class="project-gallery">
    <div class="gallery-grid">
        <div class="gallery-item">
            <img src="/assets/images/portfolio/fxpayments/images/Payment Added.png" alt="Payment added interface">
        </div>
        <div class="gallery-item">
            <img src="/assets/images/portfolio/fxpayments/images/Grouped Payments.png" alt="Grouped payments view">
        </div>
    </div>
    <p class="gallery-caption">We chose a table style design as not to deviate wildly from current systems</p>
</div>

---

## Handling Multiple Payments & Approvals

Scope expanded quickly.

The system needed to:
- Support bulk/multi-payment entry
- Enable grouped FX execution
- Require separate user approvals
- Integrate SWIFT verification for beneficiaries

This introduced new challenges:
- Duplicate beneficiary names with different SWIFT/account numbers
- Overlapping source accounts across currencies
- Multi-currency grouping logic
- Risk visibility during batch operations

<div class="project-gallery">
    <div class="gallery-grid">
        <div class="gallery-item">
            <img src="/assets/images/portfolio/fxpayments/images/Approvals.png" alt="Approval manager interface">
        </div>
        <div class="gallery-item">
            <img src="/assets/images/portfolio/fxpayments/images/Bene Manager.png" alt="Beneficiary manager">
        </div>
        <div class="gallery-item">
            <img src="/assets/images/portfolio/fxpayments/images/Error Hanlding.png" alt="Error handling states">
        </div>
    </div>
</div>

---

## Table-Based Architecture & Grouping Logic

Financial software heavily relies on table-based paradigms.

Rather than fight this convention, I leaned into it.

Using AG Grid, I designed a nested table view that grouped payments by:

- Currency
- Settlement date
- Source account

This allowed users to:
- See exposure by currency
- Understand funding allocation
- Execute grouped payments logically
- Maintain clarity during bulk operations

The grouping model preserved traditional financial UI expectations while introducing structural improvements.

<div class="project-gallery">
    <div class="gallery-grid">
        <div class="gallery-item">
            <img src="/assets/images/portfolio/fxpayments/images/Grouped Payments.png" alt="Grouped payments with nesting">
            <p class="gallery-caption">We required a grouping/nesting system for payments with the same Currency pair, Settlement Date, and Source Account</p>
        </div>
    </div>
</div>

---

## Evolving Requirements & Constraints

This was a two-year agile initiative with expanding scope.

Over time, additional requirements included:

- Detailed audit history
- Payment status tracking
- Improved beneficiary selection (beyond simple dropdowns)
- Stronger SWIFT validation workflows
- Deeper reconciliation visibility

Design decisions were shaped by:
- Regulatory expectations
- Established financial software conventions
- Technical system limitations
- Design system constraints
- Ongoing client feedback

Requests often came through the product owner after coordination with clients and adjacent product teams. I continuously balanced new requirements with existing paradigms to avoid destabilizing the system.

<div class="project-gallery">
    <div class="gallery-grid">
        <div class="gallery-item">
            <img src="/assets/images/portfolio/fxpayments/images/Adustable panels & pending approval statuses.png" alt="Adjustable panels with pending approval statuses">
        </div>
        <div class="gallery-item">
            <img src="/assets/images/portfolio/fxpayments/images/audit trail.png" alt="Audit trail view">
        </div>
        <div class="gallery-item">
            <img src="/assets/images/portfolio/fxpayments/images/Source Selection.png" alt="Source account selection">
        </div>
    </div>
</div>

---

## Key Challenges

- Integrating fragmented backend systems into a single UX
- Designing for novice clarity and expert flexibility
- Managing duplicate naming and account ambiguity
- Maintaining financial accuracy within table constraints
- Adapting to shifting requirements without creating inconsistency
- Operating within legacy system limitations

---

## Outcome

The unified application:

- Reduced operational friction across systems
- Simplified FX payment entry for treasury users
- Preserved control for experienced traders
- Enabled bulk and grouped execution
- Improved visibility into payment lifecycle and audit history
- Created a scalable foundation for future FX capabilities

---

## Reflection

This project deepened my understanding of financial software design—especially the tension between:

- Established financial paradigms
- Modern UX expectations
- Regulatory constraints
- Technical system fragmentation

Designing within these boundaries required systems thinking, negotiation, and long-term coherence—not just screen design.

The most important outcome was not a single feature—it was transforming multiple disconnected processes into a unified mental model.
