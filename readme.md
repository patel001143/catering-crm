# Shawarma Moose Catering CRM

This is an AI-powered catering customer relationship management system designed for Shawarma Moose. It automates the process of handling catering leads, generating personalized quotes using AI, sending emails, following up, and generating invoices.

## ✨ Features

- Webhook/API integration to receive leads
- Kanban-style lead management board
- AI-powered quote generation using OpenAI Codex
- Automated email generation, editing, and sending
- Smart follow-ups based on customer interaction or lack of response
- Invoice generation from confirmed quotes
- Admin login system with role-based access

## 🧱 Tech Stack

- **Backend**: Laravel (PHP 8+)
- **Database**: MySQL
- **Frontend**: Blade + Laravel Livewire (or Vue.js)
- **Email**: Mailgun or SendGrid
- **AI Layer**: OpenAI GPT-4 Turbo via API (Codex)
- **PDF Generator**: dompdf (for invoices)
- **Job Scheduling**: Laravel Scheduler
- **Deployment**: Laravel Forge + GitHub

## 🚀 Getting Started

```bash
composer install
cp .env.example .env
php artisan key:generate
php artisan migrate --seed
npm install && npm run build
php artisan serve
