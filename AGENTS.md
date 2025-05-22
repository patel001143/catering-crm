
---

## ✅ `AGENTS.md` — Codex Agent Guide

```md
# AGENTS.md — AI Agent Operating Guide

This file defines the goals, roles, and structured prompt behavior for OpenAI Codex or any AI agent working in this Laravel-based project.

---

## 🧠 Project Summary

Shawarma Moose CRM is a Laravel-based system that automates the full catering sales pipeline using Codex. The agent is responsible for generating backend logic, views, models, prompts, and tests that automate:

- Lead ingestion
- Quote generation
- Email communication
- Follow-ups
- Invoice generation

---

## 🎯 Agent Objectives

1. Generate Laravel code that automates business workflows
2. Use Shawarma Moose menu data when generating quotes
3. Write editable, human-friendly emails for customer interactions
4. Organize leads into Kanban-style stages
5. Write clean, tested code using Laravel best practices

---

## 💡 Prompting Rules for Codex

When writing prompts or receiving tasks:

### For Models & Migrations
> “Create Laravel models and migrations for leads, quotes, emails, menu_items, and invoices with soft deletes and timestamps.”

### For AI Quote Generator
> “Build a Laravel service that uses the OpenAI API to generate a catering quote using past examples and the Shawarma Moose menu.”

### For Automated Emails
> “Generate professional email templates for sending a quote, requesting details, and sending follow-ups.”

### For Follow-ups
> “Create a Laravel Job that sends AI-generated follow-up emails based on event dates and prior communication status.”

---

## ✅ Coding Standards

- Use Eloquent relationships
- Add form requests for validation
- Store AI prompt/response logs in a dedicated table
- Use enums where applicable (`status`, `quote_status`, etc.)
- Include feature tests for all endpoints and jobs

---

## 🧪 Testing Guide

- Use `php artisan test` to run all unit and feature tests
- Every new controller or service should include a basic feature test
- Quote generation and email workflows should be testable via assertions

---

## 🧠 Memory Context for Codex (optional prompt injection)

Codex should keep a context of:
- Past quotes
- Menu data (protein, sides, dips)
- Lead history (status, replies)
To personalize responses and streamline automation.

---

## ✅ Role of Human Operator

- Approve AI-generated emails/quotes before sending (unless auto mode is enabled)
- Use UI actions to send, edit, or follow up
- Provide feedback to Codex if output needs refinement
