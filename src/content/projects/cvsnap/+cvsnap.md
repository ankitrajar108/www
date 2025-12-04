---
name: CVSnap
description: ai powered professional headshots in minutes
date: 2025-08-04
icon: code
github: https://github.com/ankitrajar108/CVSnap
link: https://cvsnap.app
images: [cover.png]
published: true
---

CVSnap is a web application that generates professional headshots using AI models. Users upload a small set of photos and receive a full collection of polished, studio-quality headshots within minutes. The goal is to replace traditional photography sessions with a faster, more accessible, and more affordable alternative.

This project was built as a full SaaS product with authentication, payments, image processing, storage, and a user dashboard.

## the idea
Getting a professional headshot is more difficult than it should be. Booking a photographer, taking time out for a photoshoot, waiting for edits, and paying high fees all create friction. Many people end up using old or low-quality photos simply because the process feels inconvenient.

CVSnap solves this problem by automating the entire workflow. Users upload their photos, choose their plan, and receive a curated set of high-quality headshots that look professional and consistent. The aim was to create a simple, reliable, on-demand solution that works for students, job seekers, founders, or anyone who needs a polished image for their online presence.

## the app
CVSnap is built as a streamlined user experience.

The main dashboard guides users through uploading photos, selecting a plan, and tracking the generation progress. A status tracker updates the user as the AI model trains and produces results, ensuring the process feels transparent rather than hidden.

The AI engine uses Astria and Flux models to create high-resolution images styled for professional use. Each plan delivers a different quantity of headshots, ranging from forty to two hundred images. All generated images are stored securely for thirty days, with an option to download them individually or in bulk.

Payments are handled through Dodo, and the entire flow is tightly integrated with Supabase for authentication, database storage, and file handling. Once generation is complete, users can review and download their entire set from the dashboard.

## implementation
The application is built with Next.js as both the frontend and backend framework. Supabase handles authentication, user data, and file storage. Image generation is powered through the Astria AI API, with a workflow that creates training jobs, polls their status, retrieves the output, and stores results for user access.

The stack includes Next.js fourteen, React eighteen, TypeScript, Tailwind CSS, Supabase PostgreSQL, Supabase Auth, Supabase Storage, Astria AI, and Dodo Payments. The app is deployed on Vercel.

One of the more challenging parts was building the asynchronous pipeline for AI generation without relying on long-running server functions. Polling, background processing, and database state management were used to keep the experience smooth while avoiding timeouts.

## challenges
Coordinating the entire lifecycle of an AI training job required careful planning. Handling errors, retries, and edge cases like failed uploads or incomplete photo sets had to be built into the flow. Managing storage and enforcing the thirty-day expiration window also required automated cleanup routines.

Aligning payment webhooks with user plan states was another area that needed attention. Ensuring that the user dashboard always reflects accurate payment and generation status took several iterations.

## thoughts
CVSnap delivers a complete end-to-end product that solves a real problem. It demonstrates how AI can streamline a traditionally slow and expensive process. The final result feels polished, fast, and reliable.

There is a lot of room to build on this foundation, such as adding more styles, improving model customization, offering team accounts, or expanding into resume and profile branding tools.

Overall, CVSnap was a valuable experience in designing a production-grade AI workflow, managing real-time user progress, and building a modern full-stack SaaS product.